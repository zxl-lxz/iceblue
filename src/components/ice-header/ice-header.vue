<template>
  <div class="ice-header" id="header">
    <el-row>
      <el-col :span="24">
          <div class="main">
            <h1 class="logo"><a href="">ICE  BLUE</a></h1>
              <ul>
                <li><a href="#first">首页</a></li>
                <li><a href="#first">团队</a></li>
                <li><a href="#iceAch">成果</a></li>
                <li><a href="">关于</a></li>
                <li><a href="#join">加入</a></li>
                <li><a href="">IceHub</a></li>
              </ul>
          </div>
      </el-col>
    </el-row>
  </div>
</template>

<script type="text/javascript">
export default {
  created () {
    window.onscroll = function () {
      var scrollTop = document.body.scrollTop || document.documentElement.scrollTop
      const Ohead = document.getElementById('header')
      if (scrollTop > 700) {
        Ohead.style.background = 'rgba(255, 255, 255, 0.9)'
        Ohead.style.borderBottom = '1px solid grey'
      } else {
        Ohead.style.background = ''
        Ohead.style.borderBottom = ''
      }
    }
  }
}
</script>

<style scoped>
.ice-header {
  width: 100%;
  height: 100px;
  position: fixed;
  top: 0;
  z-index: 999;
  /*background: rgba(255,255,255,0.7);*/
  /*border-bottom: 1px solid grey;*/
}
.el-row {
  width: 100%;
  height: 100px;
  position: fixed;
  top: 0;
  left: 0;
  overflow: hidden;
}
.ice-header a:hover {
  text-decoration: none;
}
.main {
  width: 60%;
  height: 100px;
  margin: 0 auto;
}
.logo {
  height: 100px;
  float: left;
  line-height: 100px;
}
.logo a {
  font-family: 'Antique Olive';
  font-size: 36px;
  font-weight: bolder;
  color: #409eff;
}
ul {
  float: right;
  line-height: 100px;
}
ul li {
  display: inline-block;
  padding-left: 30px;
}
ul li a {
  font-size: 16px;
  color: #409eff;
}
</style>
