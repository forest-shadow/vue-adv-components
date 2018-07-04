<template>
  <button
      class="delete-account-button"
      type="button"
      @click="modalOpen = true">
    <slot></slot>

    <ConfirmDeleteModal
      :show="modalOpen"
      :account-id="accountId"
      @close="modalOpen = false"
    />
  </button>
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
      modalOpen: false
    }
  }
}
</script>
