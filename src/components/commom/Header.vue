<template>
  <mt-header :title="title" :class="colorFlag?'themeBgc ignore':'themeColor ignore'">
    <router-link to="/" slot="left" class="leftCon" v-if="back">
      <mt-button type="primary" class="headerbtn">
        <i class="mint-toast-icon mintui mintui-back"></i>
      </mt-button>
    </router-link>
    <mt-button slot="right" v-if="more" class="headerbtn">
      <i class="mint-toast-icon mintui mintui-more"></i>
    </mt-button>
  </mt-header>
</template>
<script>
export default{
  props:{
    title: String,
    back: Boolean,
    more: Boolean,
    colorFlag: Boolean
  }
}
  
</script>
<style lang="less" scoped>
  .mint-header.ignore{
    height:50px;
    font-size:20px;
    background-color:transparent;
    .headerbtn{
      height:50px;
      .mintui{
        font-size:20px;
      }
    }
    
  }
</style>