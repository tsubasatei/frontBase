<template>
    <div>
         <img :src="item.imgUrl" alt="" v-for="(item, index) in infoContent.images" :key="index" @click="changeImg(index)">
         <p class="cur">
             <img :src="infoContent.images[idx].imgUrl" alt="">
         </p>
         <p class="detail">
             <span>{{infoContent.productColor}}</span>
             <span>{{infoContent.productSize}}</span>
         </p>
    </div>
</template>

<script>
    export default {
        props:['infoContent'],
        data() {
            return {
                idx:0
            }
        },
        methods: {
            changeImg(index) {
                this.idx = index
            }
        },
    }
</script>

<style scoped>
img{
    height:60px;
    margin-right: 10px;
    cursor: pointer;
}
.cur img{
    width:300px;
}
.detail{
    font-size: 14px;
    color:#aaa
}
</style>