<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <div class="card">
        <h1 class="text-2xl font-bold mb-6">Your Contacts</h1>
        <ContactsList :contacts="contacts" />
      </div>
    </div>
  </div>
</template>

<script>
import ContactsList from "./components/ContactsList";
export default {
  name: 'app',
  components: { ContactsList },
  data() {
    return {
      contacts: [
        {
          id: 1,
          name: "Alfreda Ferreira",
          email: "alfreda.ferreira@example.com",
          avatar: "https://randomuser.me/api/portraits/med/women/6.jpg"
        },
        {
          id: 2,
          name: "Leevi Wirtanen",
          email: "leevi.wirtanen@example.com",
          avatar: "https://randomuser.me/api/portraits/med/men/19.jpg"
        },
        {
          id: 3,
          name: "Kaitlin Sutton",
          email: "kaitlin.sutton@example.com",
          avatar: "https://randomuser.me/api/portraits/med/women/2.jpg"
        },
        {
          id: 4,
          name: "Alice Wilson",
          email: "alice.wilson@example.com",
          avatar: "https://randomuser.me/api/portraits/med/women/62.jpg"
        },
        {
          id: 5,
          name: "Etienne Roy",
          email: "etienne.roy@example.com",
          avatar: "https://randomuser.me/api/portraits/med/men/4.jpg"
        }
      ]
    }
  }
}
</script>

<style src="./assets/css/app.css" />
