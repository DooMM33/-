<template>
  <div class="mainpic">
    <img class="title" src="@/assets/img/spinning/spiningtitle.png" alt="">
    <img class="spinning" src="@/assets/img/spinning/spinning.png" alt="" >
    <img class="click" src="@/assets/img/spinning/clickstart.png" alt="">
  </div>
</template>

<script>
export default {
name: "MainPic"
}
</script>

<style scoped>
.mainpic{
  position: relative;
}
.title{
  display: flex;
  margin: 0 auto;
  width:75%;
  z-index: 9;
}
.spinning{
  display: flex;
  margin:0 auto;
  width: 70%;
  z-index: 1;
}
.click{
  position: absolute;
  left: 40%;
  top:43%;
  width:20%;
}
</style>