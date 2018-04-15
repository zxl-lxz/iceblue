<template>
  <div class="ice-team" id="first">
    <el-carousel :interval="5000" arrow="always" height="100%">
        <el-carousel-item v-for="item in items" :key="item">
          <div class="img-wrapper">
            <img :src="item" >
          </div>
        </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: {
        pic1: 'http://og3j4ihx8.bkt.clouddn.com/b.jpg',
        pic2: 'http://og3j4ihx8.bkt.clouddn.com/c.jpg',
        pic3: 'http://og3j4ihx8.bkt.clouddn.com/d.jpg',
        pic4: 'http://og3j4ihx8.bkt.clouddn.com/f.jpg'
      }
    }
  }
}
</script>

<style scoped>
div {
  height: 100%;
}
.img-wrapper {
  width: 100%;
  height: 100%;
}
.el-carousel__item img {
  width: 100%;
  height: 100%;
}
</style>
