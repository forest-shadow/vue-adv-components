<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <ContactList></ContactList>
    </div>
  </div>
</template>

<script>
import ContactList from './components/ContactList'

export default {
  name: 'app',
  components: {
    ContactList
  }
}
</script>
