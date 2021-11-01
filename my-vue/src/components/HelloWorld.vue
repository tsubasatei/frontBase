<template>
  <div>
    <h1>我是HelloWorld，我接收到的父组件的值是{{valueA}}、{{valueB}}、{{valueC}}</h1>
    <button @click="add">按我加1</button>
  </div>
</template>

<script>
export default {
  props:['valueA', 'valueB', 'valueC'],
  // props:{
  //   valueA:{
  //     type:Number,
  //     required:false,
  //     default:()=>{
  //       return 500
  //     },
  //     validator:function(value) {
  //       return value > 50
  //     }
  //   },
  //   valueB:Number,
  //   valueC:{
  //     type:Number,
  //     required:false,
  //     default:()=>{
  //       return 500
  //     },
  //     validator:function(value) {
  //       return value > 50
  //     }
  //   }
  // },
  data(){
    return {}
  },
  methods: {
    add() {
      this.$emit('add');
    }
  }
}
</script>

<style scoped>

</style>
