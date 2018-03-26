<template>
  <div class="ice-header">
    <el-row>
      <el-col :span="24">
          <div class="main">
            <h1 class="logo"><a href="">ICE  BLUE</a></h1>
              <ul>
                <li><a href="">首页</a></li>
                <li><a href="">团队</a></li>
                <li><a href="">成果</a></li>
                <li><a href="">关于</a></li>
                <li><a href="">加入</a></li>
                <li><a href="">IceHub</a></li>
              </ul>
          </div>
      </el-col>
    </el-row>
  </div>
</template>

<script type="text/javascript">
export default {}
</script>

<style scoped>
.ice-header {
  width: 100%;
  height: 100px;
  position: fixed;
  top: 0;
  z-index: 999;
}
.el-row {
  width: 100%;
  height: 100px;
  position: fixed;
  top: 0;
  left: 0;
  overflow: hidden;
  z-index: 999;
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
