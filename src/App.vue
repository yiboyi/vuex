<template>
  <div id="app">
    <my-add></my-add>
    <p>-------------------------------</p>
    <my-sub></my-sub>
  </div>
</template>

<script>
import add from './components/add'
import sub from './components/sub'
export default {
  data () {
    return {}
  },
  components: {
    'my-add': add,
    'my-sub': sub
  }
}
</script>
<style scoped>
</style>
