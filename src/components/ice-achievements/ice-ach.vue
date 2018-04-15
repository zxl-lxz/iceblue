<template>
  <div class="iceAch" id="iceAch">
    <div class="title">
      <span class="we">我们</span>
      <span class="do-something">做了些什么？</span>
    </div>
    <div class="desc">
      <p class="inner">
        {{desc}}
      </p>
    </div>
    <div class="card-wrapper">
      <ul class="card">
          <li v-for="(card, index) in cardList" :key="index" @click="show = !show">
            <el-collapse-transition>
              <div class="default" v-if="!show">
                <p>{{card.defaultDesc}}</p>
                <p>{{card.english}}</p>
              </div>
            </el-collapse-transition>
            <el-collapse-transition>
              <div class="active" v-if="show">
                <p>{{card.activeDesc}}</p>
              </div>
            </el-collapse-transition>
          </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      desc: '冰蓝工作室着手于公益事业。致力于减少大学生求职困难、缓解互联网人才短缺现状、为大学生提供社会实践的平台。',
      cardList: [
        {
          defaultDesc: '珍题库APP',
          english: 'Treasures Questions App',
          activeDesc: '珍题库是一款公务员行测题库app，是冰蓝和南京大学教师合作的真对公务员真题演练的项目。珍题库的设计页面为绿色，绿色会给人一种放松的感觉。其主页面分为学习，笔记本，模拟测试，收藏夹等一系列板块，用不同的颜色区分，像win8的界面，这样依据受众对色彩的敏感程度会迅速找到自己需要的板块。'
        },
        {
          defaultDesc: '冰晶花项目',
          english: 'Ice crystal flower',
          activeDesc: '冰晶花项目是由冰蓝工作室一期优秀学员刘琦带领团队与某大学的成员组建的团队，经过不懈的努力将艺术与科技相结合得出此美的化身：冰晶花。冰晶花（Limpidity Flower）也叫水晶花、冰莹花，又叫“永不凋谢的纯真”。'
        },
        {
          defaultDesc: '触点餐',
          english: 'Touch point meal',
          activeDesc: '触点餐系统项目是由冰蓝工作室一期优秀学员龚杰带领团队，在刘俐等专业老师的指导下通过开发的一种基于二维码技术的电子点餐方法及系统。我们通过该项目实现强化学生创新创业能力的训练，增强高校学生的创新能力和在创新基础上的创业能力，培养适应创新型国家建设需要的高水平人才。'
        },
        {
          defaultDesc: '成长手册',
          english: 'manual',
          activeDesc: '《成长手册》获全国多家媒体报道，并得到省委书记的关注'
        }
      ],
      show: false
    }
  },
  methods: {
    showDetail () {
      document.getElementsByClassName('default').style.display = 'none'
      document.getElementsByClassName('active').style.display = 'block'
    },
    showDefault () {
      document.getElementsByClassName('default').style.display = 'block'
      document.getElementsByClassName('active').style.display = 'none'
    }
  }
}
</script>

<style scoped>
  .iceAch {
    width: 100%;
    height: 100%;
    text-align: center;
    border-bottom: 1px solid cornflowerblue;
  }
  .title {
    height: 100px;
    padding-top: 160px;
    line-height: 100px;
    font-size: 32px;
    font-weight: bolder;
  }
  .we {
    color: #000000;
  }
  .do-something {
    color: cornflowerblue;
    border-bottom: 3px solid cornflowerblue;
  }
  .desc {
    height: 60px;
  }
  .inner {
    width: 600px;
    height: 60px;
    margin: 0 auto;
    color: grey;
  }
  .card-wrapper {
    width: 1100px;
    height: 250px;
    margin: 0 auto;
    margin-top: 60px;
    font-size: 0;
  }
  .card {
    height: 100%;
  }
  .card li {
    display: inline-block;
    width: 250px;
    height: 100%;
    padding-right: 10px;
  }
  .card li:last-child {
    padding-right: 0;
  }
  .default {
    width: 100%;
    height: 100%;
    border: 1px solid darkgray;
    border-bottom: 3px solid cornflowerblue;
  }
  .default p {
    font-size: 22px;
    color: #000000;
    padding-top: 85px;
  }
  .default p:last-child {
    font-size: 16px;
    color: grey;
    padding-top: 10px;
  }
  .active {
    width: 100%;
    height: 100%;
    background-color: cornflowerblue;
    color: white;
  }
  .active p {
    font-size: 16px;
  }
</style>
