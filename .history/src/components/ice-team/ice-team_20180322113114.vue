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
        pic1: 'http://img5.imgtn.bdimg.com/it/u=161888459,1712714238&fm=27&gp=0.jpg',
        pic1: 'http://img5.imgtn.bdimg.com/it/u=161888459,1712714238&fm=27&gp=0.jpg',
        pic1: 'http://img5.imgtn.bdimg.com/it/u=161888459,1712714238&fm=27&gp=0.jpg',
        pic1: 'http://img5.imgtn.bdimg.com/it/u=161888459,1712714238&fm=27&gp=0.jpg'
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
</style>


