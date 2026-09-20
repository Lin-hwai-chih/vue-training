<script setup>
import { ref } from "vue";
let text = ref("主要網站內容");
let change = function () {
  text.value = "新的網站內容";
};
defineProps(["color", "backgroundColor"]);
</script>

<template>
  <main :style="{ color: color, backgroundColor: backgroundColor }">
    <div @click="change">{{ text }}</div>
  </main>
</template>
 
<style scoped>
main {
  padding: 10px;
  background-color: #dddddd;
}
</style>
