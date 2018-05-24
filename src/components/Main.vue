<template>
  <div>
    <v-header :title="title" :back="false" :more="true" :colorFlag="true"></v-header>
    <v-tabbarcon :selected="selected"></v-tabbarcon>
    <v-tabbar :selected="selected" @transferSelected="getSelected"></v-tabbar>
  </div>
</template>
<script>
import Header from "./commom/Header.vue";
import Tabbar from "./commom/Tabbar.vue"
import TabbarCon from "./commom/TabbarCon.vue"
export default{
  components:{
    'v-header':Header,
    'v-tabbar':Tabbar,
    'v-tabbarcon':TabbarCon,
  },
  data(){
    return {
      title:'首页',
      selected:'home'
    }
  },
  methods:{
    getSelected(value){
      this.selected = value
      switch (value){
        case 'home':
          this.title = '首页';
        break;
        case 'movie':
          this.title = '书影音';
        break;
        case 'broadcast':
          this.title = '广播';
        break;
        case 'group':
          this.title = '小组';
        break;
        case 'user':
          this.title = '我的';
        break;
      }
    }
  }
}
  
</script>
<style lang="less" scoped>

</style>