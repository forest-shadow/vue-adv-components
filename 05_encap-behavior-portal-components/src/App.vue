<template>
  <div id="app"
       class="min-h-screen bg-grey-darker p-8"
  >
    <div class="max-w-sm mx-auto">
      <UserSettingsForm @open:confirm-delete-modal="confirmDeleteModalOpen = true"/>
    </div>

    <ConfirmDeleteModal
      :show="confirmDeleteModalOpen"
      :account-id="accountId"
      @close="confirmDeleteModalOpen = false"
    />
  </div>
</template>

<script>
import ConfirmDeleteModal from './components/ConfirmDeleteModal.vue'
import UserSettingsForm from './components/UserSettingsForm.vue'

export default {
  name: 'app',
  components: {
    ConfirmDeleteModal,
    UserSettingsForm
  },
  data() {
    return {
      accountId: 7,
      confirmDeleteModalOpen: false
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>
