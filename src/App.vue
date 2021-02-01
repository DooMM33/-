<template>
  <div id="app">
    <img class="building" src="@/assets/img/background.png" alt="">
    <mainpic class="mainpic"/>
    <tabcontrol :showmess="['中奖纪录','活动规则','奖品设置']"
                @tabclick="tabClick"/>
    <scroll class="scrollb">
      <showlist :show-type="currentType"/>
    </scroll>
  </div>
</template>

<script>

import mainpic from '@/components/mainpic/MainPic'
import tabcontrol from '@/components/tabcontrol/TabControl'
import showlist from '@/components/showlist/ShowList'
import scroll from '@/components/betterscroll/Scroll'
export default {
  name: 'App',
  components: {
    mainpic,
    tabcontrol,
    showlist,
    scroll
  },
  data(){
    return {
      currentType:'note'
    }
  },
  methods:{
    tabClick(index){
      switch (index){
        case 0:
          this.currentType='note';
          break;
        case 1:
          this.currentType='rule';
          break;
        case 2:
          this.currentType='prize';
          break;
      }
    }
  }

}
</script>

<style scoped>
@import "./assets/css/base.css";

.building{
  width: 100%;
  height:100%;
  position: fixed;
  z-index: -1;
}
.scrollb{
  height:calc(100% - 400px);
  overflow: hidden;
}
</style>
