<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <ContactList :pseudo-slot="({ contact }) => contact.name.first">
        <a slot-scope="{ contact }"
           :href="`/contacts/${contact.id}`"
        >
          {{ contact.name.first }}
        </a>
      </ContactList>
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

<style src="./assets/css/app.css"></style>
