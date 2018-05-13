<template src="./index.html">
</template>

<script type="text/ecmascript-6">
export default {
  data () {
    return {
      teamLists: [
        {
          desc: 'This is some detail',
          img: 'http://og3j4ihx8.bkt.clouddn.com/QQ%E5%9B%BE%E7%89%8720160509114935.jpg'
        },
        {
          desc: 'This is some detail',
          img: 'http://og3j4ihx8.bkt.clouddn.com/IMG_20180513_103945.jpg'
        },
        {
          desc: 'This is some detail',
          img: 'http://og3j4ihx8.bkt.clouddn.com/QQ%E5%9B%BE%E7%89%8720180513102631.jpg'
        },
        {
          desc: 'This is some detail',
          img: 'http://og3j4ihx8.bkt.clouddn.com/QQ%E5%9B%BE%E7%89%8720180513102724.jpg'
        }
      ],
      textLists: [
        '校企合作模式',
        '环境舒适的工作室',
        '共同的学习目标',
        '专业的技术知识',
        '往届学长学姐经验指导',
        '珍贵的内推机会',
        '活跃的团建氛围',
        '有爱的教师团队'
      ]
    }
  },
  created () {
    $('.card').css('height', '10em');
  }
}
</script>

<style lang="less" src="./index.less" scoped>
</style>


