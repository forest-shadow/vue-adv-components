<template>
<form class="user-settings-form card"
      @submit.prevent="submit"
>
  <h1 class="text-2xl font-bold mb-6">Your Settings</h1>
  <label class="block mb-6">
    <span class="form-label mb-2">Email Address</span>
    <input type="text" class="form-input" placeholder="you@example.com"
           :value="email"
           @input="email = $event.target.value"
    >
  </label>
  <div class="mb-8">
    <span class="form-label mb-2">Newsletter</span>
    <div class="flex justify-between items-center">
      <p class="mr-4">Send your occasional news and updates</p>
      <toggle-input v-model="receiveNewsletter"/>
    </div>
  </div>
  <div class="text-right">
    <button class="btn btn-blue" type="submit">Update Settings</button>
  </div>
</form>
</template>

<script>
import ToggleInput from './ToggleInput'

export default {
  name: 'UserSettingsForm',
  components: { ToggleInput },
  props: [],
  data() {
    return {
      email: 'jane@example.com',
      receiveNewsletter: false
    }
  },
  methods: {
    submit() {
      // eslint-disable-next-line
      console.log('Submitting preferences...', {
        email: this.email,
        receiveNewsletter: this.receiveNewsletter
      })
    }
  }
}
</script>

<style scoped>

</style>
