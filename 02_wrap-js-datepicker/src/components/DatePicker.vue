<template>
  <div class="date-picker">
    <input type="text"
           class="form-input"
           placeholder="YYYY-MM-DD"
           ref="input"
           :value="value"
    >
  </div>
</template>

<script>
import Pikaday from 'pikaday'
import "pikaday/css/pikaday.css"

export default {
  name: 'DatePicker',
  props: {
    value: { required: true },
    format: { default: 'YYYY-MM-DD' },
    options: { default: {} }
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      format: this.format,
      onSelect: () => {
        this.$emit('input', picker.toString())
      },
      ...this.options
    })
  }
}
</script>

