<template>
  <div>
    <mt-tab-container v-model="currentSelected">
      <mt-tab-container-item id="home">
        <v-home></v-home>
      </mt-tab-container-item>
      <mt-tab-container-item id="movie">
        <v-movie></v-movie>
      </mt-tab-container-item>
      <mt-tab-container-item id="broadcast">
        broadcast
      </mt-tab-container-item>
      <mt-tab-container-item id="group">
        group
      </mt-tab-container-item>
      <mt-tab-container-item id="user">
        <v-user></v-user>
      </mt-tab-container-item>
    </mt-tab-container>
  </div>
</template>
<script>
import Home from "../Home"
import Movie from "../Movie"
import User from "../User"
  export default{
    props:{
      selected: String
    },
    components:{
      'v-home':Home,
      'v-movie':Movie,
      'v-user':User
    },
    data(){
      return {
        currentSelected:this.selected
      }
    },
    methods:{
      
    },
    watch:{
      selected(value,old){
        this.currentSelected = this.selected
      }
    }
  }
</script>
<style lang="less" scoped>
  .tabbar{
    border-top: 1px solid #ddd;
    img{
      width:50px;
      height:50px;
    }
    .title{
      font-size:26px;
      margin-top:5px;

    }
  }
  .mint-tabbar>.mint-tab-item.is-selected{
    color: #42bd56;
  }
</style>