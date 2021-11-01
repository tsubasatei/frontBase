<template>
<!-- https://club.jd.com/comment/productPageComments.action?callback=fetchJSON_comment98&productId=10037660470160&score=0&sortType=5&page=0&pageSize=10&isShadowSku=0&fold=1 -->
  <div class="box">
    <div class="left">
      <div class="pic">
        <img :src="'http://' + info.userImage" alt="" />
      </div>
      <h4>{{ info.nickname }}</h4>
    </div>
    <div class="right">
      <p
        class="star"
        :style="{ 'background-position': -16 * (5 - info.score) + 'px 0px' }"
      ></p>
      <p>{{ info.content }}</p>
      <comm-pic :info-content="info"></comm-pic>
    </div>
  </div>
</template>

<script>
import CommPic from "./CommPic.vue";
export default {
  props: ["info"],
  components: {
    CommPic,
  },
};
</script>

<style scoped>
.box {
  display: flex;
  border-bottom: 1px solid #ccc;
  margin-bottom: 15px;
}
.box .left {
  flex: 2;
}
.box .right {
  flex: 8;
}
.box .left .pic {
  height: 40px;
  width: 40px;
}
.box .left .pic img {
  height: 100%;
  width: 100%;
  border-radius: 50%;
  border: 1px solid #ccc;
}
.box .right .star {
  width: 80px;
  height: 14px;
  background: url(../assets/star.png);
}
</style>