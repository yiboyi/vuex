<template>
    <div>
      <h3>当前的值count:{{this.$store.state.count}}</h3>
      <h2>{{$store.getters.showNum}}</h2>
      <button @click="btnHandler1">+1</button>
      <button @click="btnHandler2">+N</button>
      <button @click="btnHandler3">+1 async</button>
      <button @click="btnHandler4">+N async</button>
    </div>
</template>

<script>
export default {
  data () {
    return {}
  },
  methods: {
    btnHandler1 () {
      this.$store.commit('add')
    },
    btnHandler2 () {
      // commit的作用,就是调用某个mutation函数
      this.$store.commit('addN', 3)
    },
    btnHandler3 () {
      // 触发actions 的第一种方式
      // dispatch 专门来触发actions
      this.$store.dispatch('addAsync')
    },
    btnHandler4 () {
      this.$store.dispatch('addNAsync', 5)
    }
  }

}
</script>
<style scoped>

</style>
