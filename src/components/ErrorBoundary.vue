<script>
  export default {
    name: 'ErrorBoundary',
    data() {
      return {
        error: false
      }
    },
    errorCaptured (err, vm, info) {
      this.error = true
      console.error(`[${info}]`, err)

      return false
    },
    render (h) {
      if (this.error) {
        return h('p', { style: 'color: red' }, 'An error occurred. Check console for information')
      }

      return this.$slots.default.length === 1
        ? h(this.$slots.default[0])
        : h('div', {}, this.$slots.default)
    }
  }
</script>