<template src="./index.html">
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          text: '为湖工人的互联网梦想而生',
          title: '“我们一步一个脚印，不断向前方探索”'
        },
        {
          title: '“仅仅一个想法，这个世界因此改变”',
          text: '团队的力量让一切变得从容'
        },
        {
          title: '“码出世界，精彩由我”',
          text: '专注于Web开发技术'
        }
      ]
    }
  },
  methods: {
    changeBac () {
      $('.ice-header').addClass('change-bacg')
    }
  }
}
</script>

<style lang="less" rel="stylesheet/less" src="./index.less" scoped>
</style>
