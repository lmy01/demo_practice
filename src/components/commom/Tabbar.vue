<template>
  <div>
    <!--<mt-tab-container v-model="currentSelected">
      <mt-tab-container-item id="home">
        home
      </mt-tab-container-item>
      <mt-tab-container-item id="movie">
        movie
      </mt-tab-container-item>
      <mt-tab-container-item id="group">
        search
      </mt-tab-container-item>
      <mt-tab-container-item id="user">
        user
      </mt-tab-container-item>
    </mt-tab-container>-->
    <mt-tabbar v-model="currentSelected" class="tabbar">
      <mt-tab-item id="home">
        <img src="../../assets/images/footer/ic_tab_home_normal.png" v-if="currentSelected!=='home'">
        <img src="../../assets/images/footer/ic_tab_home_active.png" v-if="currentSelected==='home'">
        <div class="title">首页</div>
      </mt-tab-item>
      <mt-tab-item id="movie">
        <img src="../../assets/images/footer/ic_tab_subject_normal.png" v-if="currentSelected!=='movie'">
        <img src="../../assets/images/footer/ic_tab_subject_active.png" v-if="currentSelected==='movie'">
        <div class="title">书影音</div>
      </mt-tab-item>
      <mt-tab-item id="broadcast">
        <img src="../../assets/images/footer/ic_tab_status_normal.png" v-if="currentSelected!=='broadcast'">
        <img src="../../assets/images/footer/ic_tab_status_active.png" v-if="currentSelected==='broadcast'">
        <div class="title">广播</div>
      </mt-tab-item>
      <mt-tab-item id="group">
        <img src="../../assets/images/footer/ic_tab_group_normal.png" v-if="currentSelected!=='group'">
        <img src="../../assets/images/footer/ic_tab_group_active.png" v-if="currentSelected==='group'">
        <div class="title">小组</div>
      </mt-tab-item>
      <mt-tab-item id="user">
        <img src="../../assets/images/footer/ic_tab_profile_normal.png" v-if="currentSelected!=='user'">
        <img src="../../assets/images/footer/ic_tab_profile_active.png" v-if="currentSelected==='user'">
        <div class="title">我的</div>
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>
<script>
  export default{
    props:{
      selected: String
    },
    mounted(){
      this.$emit("transferSelected",this.currentSelected)
    },
    data(){
      return {
        currentSelected:this.selected
      }
    },
    watch:{
      currentSelected(value,old){
        this.$emit("transferSelected",this.currentSelected)
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