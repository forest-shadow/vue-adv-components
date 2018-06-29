<template>
  <div class="min-h-screen flex items-center justify-center">
    <button type="button"
            class="btn btn-blue"
            @click="modalOpen = true"
    >
      Open Modal
    </button>

    <AnnouncementModal :show="modalOpen"
                       @close="modalOpen = false"
    />
  </div>
</template>

<script>
import AnnouncementModal from './components/AnnouncementModal'

export default {
  name: 'app',
  components: {
    AnnouncementModal
  },
  data() {
    return {
      modalOpen: false
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>
