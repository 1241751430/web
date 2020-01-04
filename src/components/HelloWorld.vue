<template>
<div class="overall">
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
    <img src="../../static/image/bd_logo1.png" alt="" class="logo">
    <el-menu-item index="1">处理中心</el-menu-item>
    <el-submenu index="2">
      <template slot="title">我的工作台</template>
      <el-menu-item index="2-1">选项1</el-menu-item>
      <el-menu-item index="2-2">选项2</el-menu-item>
      <el-menu-item index="2-3">选项3</el-menu-item>
    </el-submenu>
    <el-menu-item index="3">消息中心</el-menu-item>
    <!-- 头像 -->
    <img src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" alt="" class="avatar">
    <i class="el-icon-search"></i>
  </el-menu>
  <div class="container">
    <div class="left">
      <ul class="left_head">
        <li>PS安装包提取★</li>
        <li>腾讯课堂直播</li>
        <li>PS入门视频教程</li>
      </ul>
      <ul class="left_head">
        <li>PS安装包提取★</li>
        <li>腾讯课堂直播</li>
        <li>PS入门视频教程</li>
      </ul>
      <ul class="left_head">
        <li>PS安装包提取★</li>
        <li>腾讯课堂直播</li>
        <li>PS入门视频教程</li>
      </ul>
    </div>
    <div class="right">
      <div class="right_head">
        <div class="right_head_left">
          <el-carousel :interval="4000" type="card" height="200px">
            <el-carousel-item v-for="item in 6" :key="item">
              <h3 class="medium">{{ item }}</h3>
            </el-carousel-item>
          </el-carousel>
        </div>
        <div class="right_head_right">
          <ul>
            <li>PS安装包提取★</li>
            <li>腾讯课堂直播</li>
            <li>PS入门视频教程</li>
          </ul>
        </div>
      </div>
      <div class="right_main">
        <div class="rigth_main_name">
          <div class="right_main_left">作品案例</div>
          <div class="right_main_right">more</div>
        </div>
        <div class="rigth_main_img">
          <ul>
            <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
            <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
           <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
            <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
            <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
            <li>
              <img src="../../static/image/1.jpg" alt="">
              <div>日系胶片风</div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data() {
      return {
        activeIndex: '1',
        activeIndex2: '1',
      };
    },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
  background-color: #f2f2f2;
}
body,ul{
  padding: 0;
  margin: 0;
}
ul{
  list-style: none;
}
.overall{
  width: 100%;
}
.el-menu-demo.el-menu--horizontal.el-menu{
  z-index: 999;
  width:100%;
  height:60px;
  position:fixed;
  top:0;
  min-width: 1282px;
}
.logo{
  width: 100px;
  float: left;
}
.avatar:focus,
.el-icon-search:focus,
.logo:focus{
  outline:none
}
[class*=" el-icon-"], [class^=el-icon-] {
    font-weight: 700;
    line-height: 4;
}
.avatar{
  width: 40px;
  border-radius: 50%;
  margin-right: 50px;
  margin-top: 10px;
  float: right;
}
.el-icon-search{
   margin-right: 30px;
  float:right
}
.container{
  width: 100%;
  margin-top: 60px;
}
.left{
  width: 20%;
  height: 100%;
  margin-top: 10px;
  text-align: center;
  float: left;
}
.left_head{
  min-width: 131px;
  padding: 0;
  width: 80%;
  margin-bottom: 30px;
  list-style: none;
  display:inline-block;
  -moz-box-shadow:0px 0px 13px #B3B3B3; 
  -webkit-box-shadow:0px 0px 13px #B3B3B3; 
  box-shadow:0px 0px 13px #B3B3B3;
}
.left_head li{
  text-align: center;
  width: 100%;
  height: 50px;
  line-height: 50px;
  background-color: #fff;
  border-bottom: 1px solid #f2f2f2;
}
.right{
  width: 80%;
  height: 100%;
  float: left;
}
.right_head{
  min-width: 575px;
  height: 240px;
}
.right_head_left,
.right_head_right{
  margin-top: 20px;
  float: left;
}
.right_head_left{
  width: 70%;
}
.el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
}
.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}
.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}
.right_head_right{
  width: 30%;
}
.right_head_right ul{
  margin-left: 20px;
  width: 90%;
  text-align: center;
  background-color: #fff;
  -moz-box-shadow:0px 0px 13px #B3B3B3; 
  -webkit-box-shadow:0px 0px 13px #B3B3B3; 
  box-shadow:0px 0px 13px #B3B3B3;
}
.right_head_right li {
  height: 50px;
  width: 100%;
  line-height: 50px;
  background-color: #fff;
  border-bottom: 1px solid #f2f2f2;
  display: inline-block;
}
.right_main{
  width: 100%;
  height: 750px;
  margin-top: 10px;
  min-width: 1011px;
}
.rigth_main_name{
  width: 100%;
  height: 45px;
  line-height: 45px;
  background-color: #fff;
  -moz-box-shadow:0px 0px 13px #B3B3B3; 
  -webkit-box-shadow:0px 0px 13px #B3B3B3; 
  box-shadow:0px 0px 13px #B3B3B3;
}
.right_main .rigth_main_name .right_main_left,
.right_main .rigth_main_name .right_main_right{
  float: left;
  text-align: left;
  padding-left: 10px;
}
.right_main .rigth_main_name .right_main_left{
  width: 85%;
}
.right_main .rigth_main_name .right_main_right{
  width: 13%;
}
.rigth_main_img{
  margin-top: 10px;
}
.rigth_main_img li {
  width: 30%;
  height: 270px;
  float: left;
  margin: 15px;
  background-color: #fff;
  -moz-box-shadow:0px 0px 13px #B3B3B3; 
  -webkit-box-shadow:0px 0px 13px #B3B3B3; 
  box-shadow:0px 0px 13px #B3B3B3;
  transition: transform 0.4s
}
.rigth_main_img img{
  margin-top: 5px;
  width: 98%;
}
.rigth_main_img div{
  height: 70px;
  line-height: 70px;
}
.rigth_main_img li:hover{
  transform: translateY(-10px);
  transition: transform 0.4s
}
</style>
