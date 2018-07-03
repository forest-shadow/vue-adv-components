<template>
  <div id="app"
       class="min-h-screen bg-grey-darker p-8"
  >
    <div class="max-w-sm mx-auto">
      <UserSettingsForm
          :account-id="accountId"
      />
    </div>

    <portal-target name="modals"></portal-target>
  </div>
</template>

<script>
import UserSettingsForm from './components/UserSettingsForm.vue'

export default {
  name: 'app',
  components: {
    UserSettingsForm
  },
  data() {
    return {
      accountId: 7
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>
