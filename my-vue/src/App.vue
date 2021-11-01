<template>
  <div>
    <one-comment v-for="(item, index) in commentArr" :key="index" :info="item">{{item}}</one-comment>
    <hello></hello>
    <hello-world @add="sumNum" :value-a="a" :value-b="b" :value-c="c"></hello-world>
  </div>
</template>

<script>
import OneComment from './components/OneComment.vue'
import HelloWorld from './components/HelloWorld.vue'
import Hello from './components/Hello.vue'

import comments from './comments'

export default {
  name: 'App',
  components: {
    OneComment,
    Hello,
    HelloWorld
  },
  data(){
    return {
      a:100,
      b:200,
      c:300,

      commentArr: comments
    }
  },
  methods:{
    sumNum(){
      console.log("123")
      this.a++
    }
  }
}
</script>

<style>

</style>
