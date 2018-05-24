<template>
  <div>
    <div class="loginCon">
      <div class="avaterCon">
        <div class="avater centerY">
          <img src="../assets/images/mine/avatar_male_100.png">
        </div>
        <div class="login centerY">
          <router-link to="/login">登录/注册</router-link>
        </div>
      </div>
    </div>
    <div>
      提醒：提醒：提醒：提醒：提醒：提醒：提醒：
    </div>
  </div>
  
</template>
<script>
  export default{
    data(){
      return {

      }
    }
  }
</script>
<style lang="less" scoped>
.loginCon{
  height:250px;
  text-align:center;
  background-image:url(../assets/images/mine/live_player_bg.jpg);
  background-size:100% 250px;
  .avaterCon{
    height:250px;
    position:relative;
    .avater{
      width:140px;
      height:140px;
      border-radius:50%;
      margin-left: 150px;
      img{
        width:140px;
        height:140px;
        border-radius:50%;
      }
    }
    .login{
      width:250px;
      height:80px;
      line-height:80px;
      margin-left: 350px;
      border: 1px solid #fff;
      a{
        color:#fff;
        text-decoration: none;
      }
    }
  }
}
</style>