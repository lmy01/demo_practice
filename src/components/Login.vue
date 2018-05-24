<template>
  <div >
    <v-header :back="true" :more="false" :colorFlag="false"></v-header>
    <div>
      <p class="themeColor">欢迎来到豆瓣</p>
      <input placeholder="请输入邮箱" type="email" v-model="username"></input>
      <input placeholder="请输入密码" type="password" v-model="password"></input>
      <div class="loginBtn">
        <mt-button type="primary" size="large" @click.native="handleClick" class="themeBgc">登&nbsp;&nbsp;&nbsp;&nbsp;录</mt-button>
      </div>
      <div class="register"><span class="themeColor">注册豆瓣</span><span>|</span><span>忘记密码</span></div>
    </div>
  </div>
</template>
<script>
import Header from "./commom/Header.vue";
export default{
  components:{
    'v-header':Header,
  },
  data(){
    return {
      username:'',
      password:''
    }
  },
  methods:{
    handleClick(){
      
    }
  }
}
  
</script>
<style lang="less" scoped>
  p{
    font-size:50px;
    margin-top:200px;
    margin-bottom:100px;
  }
  input{
    width:95%;
    font-size:30px;
    border:transparent;
    border-bottom:1px solid #ccc;
    margin-bottom:60px;
    outline:none;
  }
  .loginBtn{
    height:70px;
    padding:20px;
    .mint-button{
      height:100%;
      font-size:32px;
    }
  }
  .register{
    font-size:28px;
    span{
      color:#999;
      margin-right:20px;
    }
  }
</style>