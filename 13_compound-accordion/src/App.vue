<template>
  <div id="app" class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <AccordionList>
        <AccordionItem :item-id="1">
          <template slot="header">
            Item A
          </template>
          <template slot="content">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab accusantium corporis distinctio facilis molestias nesciunt omnis perspiciatis sapiente ut vel.
          </template>
        </AccordionItem>
        <AccordionItem :item-id="2">
          <template slot="header">
            Item B
          </template>
          <template slot="content">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum dignissimos eos explicabo necessitatibus nemo odit quaerat quisquam quod.
          </template>
        </AccordionItem>
        <AccordionItem :item-id="3">
          <template slot="header">
            Item C
          </template>
          <template slot="content">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum dignissimos eos explicabo necessitatibus nemo odit quaerat quisquam quod.
          </template>
        </AccordionItem>
      </AccordionList>
    </div>
  </div>
</template>

<script>
import AccordionList from './components/AccordionList.vue'
import AccordionItem from './components/AccordionItem.vue'

export default {
  name: 'app',
  components: {
    AccordionList,
    AccordionItem
  }
}
</script>

<style src="./assets/css/app.css" />
