<template src="./index.html">
</template>

<script type="text/ecmascript-6">
export default {
  data () {
    return {
    }
  },
  created () {
    window.onmousewheel = function () {
      if ($('.ice-team').offset().top < (window.innerHeight)/2) {
        $('.ice-header').addClass('change-bacg')
      } else {
        $('.ice-header').removeClass('change-bacg')
      }
    }
  },
  methods: {
    changeBac () {
      $('.ice-header').addClass('change-bacg')
    },
    backChange () {
      $('.ice-header').removeClass('change-bacg')
    },
    expectPlease () {
      this.$alert('敬请期待', '温馨提示', {
        confirmButtonText: '确定'
      });
    }
  },
  watch: {
  }
}
</script>

<style lang="less" rel="stylesheet/less" src="./index.less" scoped>
</style>
