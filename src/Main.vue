<script setup>
// import { ref } from "vue";
// import { onMounted, onUpdated, onUnmounted, ref } from "vue";
import { onMounted, onUnmounted, ref } from "vue";
// onMounted(function () {
//   console.log("組件掛載完成");
// });
// onUpdated(function () {
//   console.log("組件更新完成");
// });
// onUnmounted(function () {
//   console.log("組件卸載完成");
// });
let text = ref("主要網站內容");
let changeText = function () {
  text.value = "新的網站內容";
};
//製作一個Counter數數的功能
let counter = ref(0);
let scheduleId;
//組件掛載的時候，設定每秒鐘加1的排程
onMounted(function () {
  scheduleId = window.setInterval(function () {
    console.log("每隔一秒鐘，數字加1");
    counter.value = counter.value + 1;
  }, 1000);
});
//組件卸載的時候，清除掛載設定的排程
onUnmounted(function () {
  //清除排程
  window.clearInterval(scheduleId);
});
</script>

<template>
  <main>
    <div>{{ counter }}</div>
    <div>{{ text }}</div>
    <button @click="changeText">改變內容文字</button>
  </main>
</template>
 
<style scoped>
main {
  padding: 10px;
  background-color: #dddddd;
}
</style>
