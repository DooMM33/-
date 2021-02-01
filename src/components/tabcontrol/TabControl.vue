<template>
  <div class="tabcontrol">
    <div class="tab-control-item" v-for="(item,index) in showmess"
          :class="{active:index===currentIndex}"
          @click="tabClick(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBar",
  data(){
    return {
      currentIndex:0,
      active:false
    }
  },
  props:{
    showmess:{
      type:Array,
      default(){
        return []
      }
    }
  },
  methods:{
    tabClick(index){
      this.currentIndex=index
      this.$emit('tabclick',index)
    }
  }
}
</script>

<style scoped>
  .tabcontrol{
    display:flex;
    text-align: center;
    height:40px;
    line-height: 40px;
    background-color: darkslateblue;
    margin-top: 12%;
  }
  .tab-control-item{
    flex: 1;
  }
  .tab-control-item span{
    padding: 7px;
    color:#ffffff;
  }
  .active span{
    color:orange;
    border-bottom: 4px solid red;
  }
</style>