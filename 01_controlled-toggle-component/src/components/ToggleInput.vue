<template>
  <span class="toggle flex-no-shrink" role="checkbox" tabindex="0"
        :aria-checked="toggled.toString()"
        @click="toggle"
        @keydown.space.prevent="toggle"
  ></span>
</template>

<script>
export default {
  name: 'ToggleInput',
  model: {
    prop: 'toggled',
    event: 'toggle'
  },
  props: ['toggled'],
  methods: {
    toggle() {
      console.warn()
      this.$emit('toggle', !this.toggled)
    }
  }
}
</script>
