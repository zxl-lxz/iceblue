<template>
  <div class="ice-team">
    <el-carousel :interval="5000" arrow="always" height="100%">
        <el-carousel-item v-for="item in items" :key="item">
            <img :src="item">
        </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script type="text/ecmascript6">
export default {
  data() {
    return {
      items: {
        pic1: '../assets/img/Koala.jpg',
        pic1: '../assets/img/Koala.jpg',
        pic1: '../assets/img/Koala.jpg',
        pic1: '../assets/img/Koala.jpg'
      }
    }
  }
}
</script>

<style scoped>
.el-carousel__item img {
  width: 100%;
  height: 100%;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>


