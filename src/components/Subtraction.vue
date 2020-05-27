<template>
  <div>
    <!-- <h2>当前最新的count值{{count}}</h2> -->
    <h1>{{showNum}}</h1>
    <button @click="handel1">-1</button>
    <button @click="subN(3)">-N</button>
    <button @click="subAsync">延时-1</button>
    <button @click="subNAsync(3)">延时-N</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'
export default {
  data() {
    return {}
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNum'])
  },
  methods: {
    ...mapMutations(['sub', 'subN']),
    ...mapActions(['subAsync', 'subNAsync']),
    handel1() {
      this.sub()
    }
  }
}
</script>


<style lang="less" scoped>
</style>