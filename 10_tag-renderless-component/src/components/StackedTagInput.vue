<template>
  <RenderlessTagInput :tags="tags"
                      :remove-on-backspace="false"
                      @update="(newTags) => $emit('update', newTags)"
  >
    <div class="stacked-tag-input" slot-scope="{ tags, addTag, removeButtonEvents, inputProps, inputEvents }">
      <div class="stacked-tag-input-form">
        <input type="text" class="form-input" placeholder="Add tag..."
               v-bind="inputProps"
               v-on="inputEvents"
        >
        <button class="btn btn-indigo"
                @click="addTag"
        >Add Tag</button>
      </div>
      <ul class="stacked-tag-list">
        <li v-for="tag in tags" :key="tag">
          <span>{{ tag }}</span>
          <button class="stacked-tag-link" type="button"
                  v-on="removeButtonEvents(tag)"
          >
            Remove
          </button>
        </li>
      </ul>
    </div>
  </RenderlessTagInput>
</template>

<script>
import RenderlessTagInput from './RenderlessTagInput'

export default {
  name: 'InlineTagInput',
  components: {
    RenderlessTagInput
  },
  model: {
    prop: 'tags',
    event: 'update'
  },
  props: {
    tags: { required: true }
  }
}
</script>
