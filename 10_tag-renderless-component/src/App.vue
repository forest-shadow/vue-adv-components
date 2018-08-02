<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="card max-w-sm mx-auto mt-8">
      <label class="form-label mb-2">Renderless Stacked Layout</label>
      <StackedTagInput v-model="tags"></StackedTagInput>
    </div>

    <div class="card max-w-sm mx-auto mt-8">
      <label class="form-label mb-2">Inline Tag Input</label>
      <InlineTagInput v-model="tags"></InlineTagInput>
    </div>

    <div class="card max-w-sm mx-auto mt-8">
      <label class="form-label mb-2">Original Tag Input</label>
      <TagInput v-model="tags"></TagInput>
    </div>
  </div>
</template>

<script>
import TagInput from './components/TagInput'
import RenderlessTagInput from './components/RenderlessTagInput'
import InlineTagInput from './components/InlineTagInput'
import StackedTagInput from './components/StackedTagInput'

export default {
  name: 'app',
  components: {
    TagInput,
    RenderlessTagInput,
    StackedTagInput,
    InlineTagInput
  },
  data() {
    return {
      tags: ['awesome', 'excellent', 'amazing']
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>