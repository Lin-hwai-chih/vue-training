<script setup>
import { ref } from "vue";
// let title = "網站標題";
// let title = ref("網站標題");
let state = ref({
  title: "網站標題",
  className: "title",
});
let handle = function () {
  // console.log("點擊");
  // title = "新的網站標題";
  // title.value = "新的網站標題";
  state.value.title = "新的網站標題";
  state.value.className = "title highlight";
};
</script>

<template>
  <nav>基本的導覽列</nav>

  <main>
    <!-- <div>{{ title }}</div> -->
    <div :class="state.className">{{ state.title }}</div>
    <button @click="handle">按鈕</button>
  </main>
</template>
 
<style scoped>
main {
  background-color: #dddddd;
}
.title {
  font-weight: bold;
}
.highlight {
  color: red;
}
</style>
