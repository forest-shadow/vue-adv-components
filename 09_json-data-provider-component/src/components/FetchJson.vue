<script>
import axios from 'axios'

export default {
  name: 'FetchJson',
  props: ['url'],
  data() {
    return {
      json: null,
      loading: true
    }
  },
  created() {
    axios.get(this.url)
      .then(response => {
        setTimeout(() => {
          this.json = response.data
          this.loading = false
        }, 2000)
      })
  },
  render() {
    return this.$scopedSlots.default({
      json : this.json,
      loading: this.loading
    })
  }
}
</script>
