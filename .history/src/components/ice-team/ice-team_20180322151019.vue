<template>
  <div class="ice-team">
    <el-carousel :interval="5000" arrow="always" height="100%">
        <el-carousel-item v-for="item in items" :key="item">
          <div class="img-wrapper" v-popover:popover1>
            <img :src="item" >
          </div>
        </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script type="text/ecmascript6">
export default {
  data() {
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
.img-wrapper {
  width: 100%;
  height: 100%;
}
.el-carousel__item img {
  width: 100%;
  height: 100%;
}
</style>


