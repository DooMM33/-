<template>
  <div id="app">
    <div id="building"/>
    <mainpic/>
    <tabcontrol :showmess="['中奖纪录','活动规则','奖品设置']"/>
  </div>
</template>

<script>

import mainpic from '@/components/mainpic/MainPic'
import tabcontrol from '@/components/tabcontrol/TabControl'
export default {
  name: 'App',
  components: {
    mainpic,
    tabcontrol
  }
}
</script>

<style scoped>
@import "./assets/css/base.css";
  #building{
    background-image: url("./assets/img/background.png");
    width: 100%;
    height: 100%;
    position: fixed;
    background-size: 100% 100%;
    z-index: -1;
  }
</style>
