<template>
  <div class="delete-account-button">
    <button type="button"
            class="text-red-dark hover:underline"
            @click="confirmDeleteModalOpen = true"
    >
      Delete Account
    </button>

    <portal to="modals"
            v-if="confirmDeleteModalOpen"
    >
      <ConfirmDeleteModal
          :show="confirmDeleteModalOpen"
          :account-id="accountId"
          @close="confirmDeleteModalOpen = false"
      />
    </portal>
  </div>
</template>

<script>
import ConfirmDeleteModal from './ConfirmDeleteModal'

export default {
  name: "DeleteAccountButton",
  components: {
    ConfirmDeleteModal
  },
  props: ['accountId'],
  data() {
    return {
      confirmDeleteModalOpen: false
    }
  }
}
</script>

<style scoped>

</style>