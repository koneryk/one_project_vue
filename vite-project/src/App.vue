<script setup>
  let  one = document.getElementById("one")
  let  two = document.getElementById("two")
  console.log(one)
  console.log(two)
  


</script>

<template>
  <div class="box">
    <div id ="one" class="one"></div>
    <div id ="two" class="two"></div>
    <div class="three"></div>
    <div class="four"></div>
    <div class="five"></div>
    <div class="six"></div>
    <div class="seven"></div>
    <div class="eith"></div>
    <div class="nine"></div>
    <div class="ten"></div>
  </div>
  <button></button>
 
</template>

<style scoped>
.box{
  display: flex;
  justify-content: space-evenly;
  flex-direction: row;
}
.one{
  height: 30px;
  width: 30px;
  background: red;
}
.two{
  height: 30px;
  width: 30px;
  background: blue;
}
.three{
  height: 30px;
  width: 30px;
  background: aqua;
}
.four{
  height: 30px;
  width: 30px;
  background: salmon;
}
.five{
  height: 30px;
  width: 30px;
  background: hotpink;
}
.six{
  height: 30px;
  width: 30px;
  background: salmon;
}
.seven{
  height: 30px;
  width: 30px;
  background: skyblue;
}
.eith{
  height: 30px;
  width: 30px;
  background: saddlebrown;
}
.nine{
  height: 30px;
  width: 30px;
  background: khaki;
}
.ten{
  height: 30px;
  width: 30px;
  background: green;
}
</style>
