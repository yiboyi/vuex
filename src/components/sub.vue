<template>
  <div>
    <h3>当前的count的值:{{count}}</h3>
    <h2>{{showNum}}</h2>
    <button @click="btnHandler1">-1</button>
    <button @click="btnHandler2">-N</button>
    <button @click="btnHandler3">-1 Async</button>
    <button @click="btnHandler4">-N Async</button>

  </div>
</template>

<script>
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'
export default {
  data () {
    return {}
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNum'])

  },
  methods: {
    ...mapMutations(['sub', 'subN']),
    ...mapActions(['subAsync', 'subNAsync']),
    btnHandler1 () {
      this.sub()
    },
    btnHandler2 () {
      this.subN(3)
    },
    btnHandler3 () {
      this.subAsync()
    },
    btnHandler4 () {
      this.subNAsync(3)
    }
  }
}
</script>
<style scoped>
</style>
