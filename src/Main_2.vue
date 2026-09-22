<script setup>
import { ref } from "vue";
defineProps(["color", "backgroundColor"]);
let text = ref("主要網站內容");
let change = function () {
  text.value = "新的網站內容";
};
let emit = defineEmits(["update"]);
let updateParentSubtitle = function () {
  emit("update");
};
</script>

<template>
  <main :style="{ color: color, backgroundColor: backgroundColor }">
    <div @click="change">{{ text }}</div>
    <!-- <button @click="updateSubtitle">改變副標題</button> -->
    <!-- <button @click="$emit('update')">改變副標題</button> -->
    <button @click="updateParentSubtitle">改變副標題</button>
  </main>
</template>
 
<style scoped>
main {
  padding: 10px;
  background-color: #dddddd;
}
</style>
