<template>
  <div>
    <div v-for="item in rules" class="rules">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Rule",
  data(){
    return {
      rules:[
          '1.所购产品为Alibaba指定产品',
          '2.活动所得入场券不得转赠，不提供发票',
          '3.本活动需要实名认证',
          '4.活动更多规则致电4008515151',
          '5.活动时间:长期有效'
      ]
    }
  }
}
</script>

<style scoped>
 .rules{
   margin:6%;
   color:red;
   display: block;
 }
</style>