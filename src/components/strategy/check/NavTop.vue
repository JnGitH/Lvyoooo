<!--上面导航-->
<template>

<!--<div class="row">-->

  <!--导航-->
  <div class="container-fluid" style="margin: 0;padding: 0">
    <div class="row text-center " style="background: darkred;margin: 0;padding: 0;width: 100%;">
      <div class="col-lg-1 visible-lg"></div>

      <!--图标-->

      <div class="col-lg-1 col-md-1 col-sm-1 col-xs-2">
        <!--转至首页-->
        <a href="#">
          <!--<img  class="logo" src="../assets/logo.png" alt="">-->
        </a>


      </div>

      <div class="col-lg-1 col-md-1 col-sm-2 col-xs-2 hasborder">
          <router-link to="/">
          <a href="#">
            首页
          </a>
          </router-link>
      </div>

      <!--游记-->
      <div class="col-lg-1 col-md-1 col-sm-2 col-xs-2 hasborder">
          <a href="#">
            游记
          </a>
      </div>

      <!--旅游攻略-->
      <div class="col-lg-1 col-md-2 col-sm-2 col-xs-3 hasborder">
          <a href="#">
            旅游攻略
          </a>

      </div>
      <div class="col-lg-1  col-md-2 col-sm-1 hidden-xs"></div>
      <div class="col-lg-1  visible-lg "></div>
      <!--搜索框-->
      <div class="col-lg-3  col-md-4 hidden-xs form-group search" style="margin-top: 11px">
        <input type="text" class="input-form-control " id="search" >
      </div>
      <!--头像-->
      <div class="col-lg-1 col-md-1 hidden-sm hidden-xs" >
        <img src="../../../assets/strategy/face.jpeg" alt="" class="img-circle" id="img-face">

        <div class="hover-div" >
          <ul class="list-unstyled hover-ul" >
            <li>我的关注</li>
            <li>我的收藏</li>
            <li>我的游记</li>
            <li>写游记</li>
            <li>写攻略</li>
            <li>退出</li>
          </ul>
        </div>

      </div>

      <div class="col-lg-1 visible-lg"></div>
    </div>
    <div class="line"></div>
  </div>



<!--</div>-->
</template>

<!--复制模板-->

<script>
export default {
  name: 'NavTop',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}

</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

/*路线超链接下划线*/
.a-none-line a{
  text-decoration: none !important;
}

/*导航start*/
.row{
  line-height: 58px;
}

/*头像*/
#img-face{
  width: 58px;
  height: 58px;
  padding: 13px;
}

.hover-div{
  width: 210px;
  height: 346px;
  opacity: 0.5;
  background: #4cae4c;
  display: none;
  position: absolute;
  z-index: 5;
  left: -20%;
  top: 60px;
}
/*悬浮div*/
#img-face:hover + .hover-div{
  display: block;
}
.hover-div:hover{
  display: block;
}

.hover-ul li:hover{
  background-color: #ff9d00;
}

/*导航块*/
.hasborder:hover{
  border:2px solid #ff9d00;
  border-top:none;
  border-left: none;
  border-right: none;
  cursor: pointer;
  color: #ff9d00;
}

/*搜索框*/
.search{
  display: flex;
  justify-content: flex-end;
}

.input-form-control{
  /*圆角*/
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;
  border-bottom-right-radius:5px;
  border-bottom-left-radius:5px;

  background-color:#EFEFEF;
  border: none;
  width: 60%;
  height: 30px;
  transition: width 0.5s;
  background-image: url("../../../assets/strategy/search2.svg");
  background-repeat: no-repeat;
  background-position: 95%;
}
.input-form-control:focus{
  outline-style: none;
  transition: width 1s;
  width: 100%;
  text-shadow: none;
  -webkit-appearance: none;
  -webkit-user-select: text;
  outline-color: transparent;
  box-shadow: none;
  border:1px solid #ff9d00;
  background: url("../../../assets/strategy/search3.png");
  background-position: 95%;
  background-repeat: no-repeat;
}

.search{
  display: flex;
  justify-content: flex-end;
}
/*导航end*/
</style>
