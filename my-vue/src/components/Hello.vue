<template>
  <div>
    <h1>{{msg}} {{a}}</h1>
    <button @click="add">点我加1</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      msg:'Hello Vue',
      a:100
    }
  },
  methods: {
    add() {
      this.a++
    }
  }
}
</script>

<style scoped>

</style>
