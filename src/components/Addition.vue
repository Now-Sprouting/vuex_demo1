<template>
  <div>
    <!-- <h2>当前最新的count值{{$store.state.count}}</h2> -->
    <h1>{{$store.getters.showNum}}</h1>
    <button @click="handel1">+1</button>
    <button @click="handel2">+N</button>
    <button @click="handel3">延时+1</button>
    <button @click="handel4">延时+N</button>
  </div>
</template>

<script>
export default {
  methods: {
    handel1() {
      this.$store.commit('add')
    },
    handel2() {
      this.$store.commit('addN', 3)
    },
    handel3() {
      this.$store.dispatch('addAsync')
    },
    handel4() {
      this.$store.dispatch('addNAsync', 3)
    }
  }
}
</script>


<style lang="less" scoped>
</style>