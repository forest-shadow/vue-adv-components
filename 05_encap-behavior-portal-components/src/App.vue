<template>
  <div id="app"
       class="min-h-screen bg-grey-darker p-8"
  >
    <div class="max-w-sm mx-auto">
      <UserSettingsForm
          :account-id="accountId"
      />
    </div>

    <portal to="modals"
            v-if="showAnnouncement"
    >
      <AnnouncementModal
        :show="showAnnouncement"
        @close="showAnnouncement = false"
      />
    </portal>

    <portal-target name="modals"></portal-target>
  </div>
</template>

<script>
import AnnouncementModal from './components/AnnouncementModal.vue'
import UserSettingsForm from './components/UserSettingsForm.vue'

export default {
  name: 'app',
  components: {
    AnnouncementModal,
    UserSettingsForm
  },
  data() {
    return {
      accountId: 7,
      showAnnouncement: true
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>
