<script>
  export default {
    inject: ['sortableListItemClass'],
    name: 'SortableItem',
    mounted() {
      this.$el.classList.add(this.sortableListItemClass)
    },
    render() {
      return this.$slots.default[0]
    }
  }
</script>
