<template>
  <div class="announcement-modal modal-backdrop"
       v-show="show"
  >
    <div class="modal">
      <h1 class="text-center text-2xl font-bold mb-4">Exciting new features are here!</h1>

      <p class="text-center text-grey-darker mb-6">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab cumque in incidunt natus, quibusdam vel velit. Illo molestias qui repellat.</p>

      <div class="text-center">
        <button type="button"
                class="btn btn-blue"
                @click="dismiss"
        >
          Dismiss
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AnnouncementModal",
  props: ['show'],
  created() {
    const escapeHandler = (e) => {
      if (e.key === 'Escape' && this.show) {
        this.dismiss()
      }
    }

    document.addEventListener('keydown', escapeHandler)
    this.$once('hook:destroyed', () => {
      document.removeEventListener('keydown', escapeHandler)
    })
  },
  methods: {
    dismiss() {
      this.$emit('close')
    }
  }
}
</script>