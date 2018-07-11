<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto mb-8">
      <FetchJson url="/albums.json">
        <div class="card" slot-scope="{ json: albums, loading }">
          <h1 class="text-2xl font-bold mb-6">Top Death Metal Albums</h1>
          <div v-if="loading" class="text-grey-darker">
            Loading...
          </div>
          <div v-else>
            <div class="album-grid">
              <div class="album-grid-item" v-for="album in albums" :key="album.id">
                <img :src="album.artwork" class="" alt="">
                <h2 class="album-title">{{ album.title }}</h2>
                <p class="album-artist">{{ album.artist }}</p>
              </div>
            </div>
          </div>
        </div>
      </FetchJson>
    </div>
    <div class="max-w-sm mx-auto">
      <FetchJson url="/contacts.json">
        <div class="card" slot-scope="{ json: contacts, loading }">
          <h1 class="text-2xl font-bold mb-6">Your Contacts</h1>
          <div v-if="loading">Loading...</div>
          <div v-else>
            <div v-for="contact in contacts" :key="contact.id" class="flex items-center spaced-y-6">
              <img :src="contact.picture.medium" class="h-12 w-12 rounded-full block mr-2" alt="">
              <div>
                <div class="font-bold">
                  {{ contact.name.first }} {{ contact.name.last }}
                </div>
                <div class="text-grey-dark">
                  {{ contact.email }}
                </div>
              </div>
            </div>
          </div>
        </div>
      </FetchJson>
    </div>
  </div>
</template>

<script>
import FetchJson from './components/FetchJson'

export default {
  name: 'app',
  components: {
    FetchJson
  }
}
</script>

<style src="./assets/css/app.css"></style>