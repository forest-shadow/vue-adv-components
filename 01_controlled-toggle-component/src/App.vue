<template>
  <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <UserSettingsForm/>
    </div>
  </div>
</template>

<script>
import UserSettingsForm from './components/UserSettingsForm.vue'

export default {
  name: 'app',
  components: {
    UserSettingsForm
  }
}
</script>

<style src="./assets/css/app.css"></style>
