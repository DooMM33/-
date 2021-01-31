<template>
  <div id="app">
    <div id="building"/>
    <mainpic/>
  </div>
</template>

<script>

import mainpic from '@/components/mainpic/MainPic'
export default {
  name: 'App',
  components: {
    mainpic
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
