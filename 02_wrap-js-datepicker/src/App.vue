<template>
  <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <div class="card">
        <label class="block">
          <span class="form-label mb-2">Select a date</span>
          <DatePicker v-model="date"
                      format="MMM D YYYY"
                      :options="{ firstDay: 1 }"
          />
        </label>
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from './components/DatePicker'

export default {
  name: 'app',
  components: { DatePicker },
  data() {
    return {
      date: 'Apr 12 2018'
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>
