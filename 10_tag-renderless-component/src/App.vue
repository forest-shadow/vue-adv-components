<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="card max-w-sm mx-auto mt-8">
      <label class="form-label mb-2">Renderless Stacked Layout</label>

      <div class="stacked-tag-input-form">
        <input type="text" class="form-input" placeholder="Add tag...">
        <button class="btn btn-indigo">Add Tag</button>
      </div>
      <ul class="stacked-tag-list">
        <li>
          <span>sample-tag</span>
          <button class="stacked-tag-link" type="button">
            Remove
          </button>
        </li>
      </ul>
    </div>

    <div class="card max-w-sm mx-auto mt-8">
      <label class="form-label mb-2">Renderless Tag Input</label>
      <RenderlessTagInput v-model="tags">
        <div class="tag-input" slot-scope="{ tags, removeTag, removeButtonEvents, inputProps, inputEvents }">
          <span v-for="tag in tags" :key="tag" class="tag-input-tag">
            <span>{{ tag }}</span>
            <button type="button"
                    class="tag-input-remove"
                    v-on="removeButtonEvents(tag)"
            >
              &times;
            </button>
          </span>
          <input class="tag-input-text"
                 placeholder="Add tag..."
                 v-bind="inputProps"
                 v-on="inputEvents"
          />
        </div>
      </RenderlessTagInput>
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

export default {
  name: 'app',
  components: {
    TagInput,
    RenderlessTagInput
  },
  data() {
    return {
      tags: ['awesome', 'excellent', 'amazing']
    }
  }
}
</script>

<style src="./assets/css/app.css"></style>