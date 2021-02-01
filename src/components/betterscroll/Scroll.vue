<template>
  <div class="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>


<script>
import BScroll from '@better-scroll/core'
export default {
  name: "Scroll",
  data(){
    return {
      scroll:null
    }
  },
  mounted() {
    this.scroll=new BScroll('.wrapper',{
      scrollY:true,
      observeDOM:true,
      pullUpLoad:true
    })
  }
}
</script>

<style scoped>

</style>