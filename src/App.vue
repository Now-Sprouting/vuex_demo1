<template>
  <dir>
    <my-addition></my-addition>
    <p>-----------------------</p>
    <my-substraction></my-substraction>
  </dir>
</template>

<script>
import Addition from './components/Addition'
import Subtraction from './components/Subtraction'
export default {
  data() {
    return {}
  },
  components: {
    'my-addition': Addition,
    'my-substraction': Subtraction
  }
}
</script>

<style lang="less" scoped>
</style>
