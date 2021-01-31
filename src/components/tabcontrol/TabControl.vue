<template>
  <div class="tabcontrol">
    <div class="tab-control-item" v-for="item in showmess">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBar",
  props:{
    showmess:{
      type:Array,
      default(){
        return []
      }
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
    padding: 5px;
    color:#ffffff;
  }
</style>