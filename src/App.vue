<script setup>
import NavComp from "./Nav.vue";
import MainComp from "./Main.vue";

import { ref } from "vue";
let subtitle = ref("這是網站的副標題");
let updateSubtitle = function () {
  subtitle.value = "這是新的副標題";
};
</script>

<template>
  <NavComp title="這是網站標題" :subtitle="subtitle"></NavComp>
  <!-- <div>{{ subtitle }}</div> -->
  <MainComp
    color="white"
    backgroundColor="black"
    @update="updateSubtitle"
  ></MainComp>
</template>
 
<style scoped>
</style>
