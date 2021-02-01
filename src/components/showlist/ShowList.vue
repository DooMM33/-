<template>
  <div class="show-list-item">
    <div v-if="showType=='prize'"><prize/></div>
    <div v-else-if="showType=='note'"><note/></div>
    <div v-else><rule/></div>
  </div>
</template>

<script>
import note from './Note'
import rule from './Rule'
import prize from './Prize'
export default {
  name: "ShowList",
  props:{
    showType:{
      type:String,
      default:'prize'
      }
    },
  components:{
    note,
    rule,
    prize
  }

}
</script>

<style scoped>

</style>