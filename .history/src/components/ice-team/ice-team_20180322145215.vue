<template>
  <div class="ice-team">
    <el-carousel :interval="5000" arrow="always" height="100%">
        <el-carousel-item v-for="item in items" :key="item">
          <div class="img-wrapper" v-popover:popover1>
            <img :src="item" >
          </div>
          <el-popover
              ref="popover1"
              placement="top-start"
              title="标题"
              width="200"
              trigger="hover"
              content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
          </el-popover>
        </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script type="text/ecmascript6">
export default {
  data() {
    return {
      items: {
        pic1:
          'http://img5.imgtn.bdimg.com/it/u=3142081627,4151929064&fm=27&gp=0.jpg',
        pic2:
          'http://img5.imgtn.bdimg.com/it/u=3142081627,4151929064&fm=27&gp=0.jpg',
        pic3:
          'http://img5.imgtn.bdimg.com/it/u=3142081627,4151929064&fm=27&gp=0.jpg',
        pic4:
          'http://img5.imgtn.bdimg.com/it/u=3142081627,4151929064&fm=27&gp=0.jpg'
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


