<script setup>
defineProps(["title"]);
</script>

<template>
  <!-- <nav>基本的導覽列</nav> -->
  <nav>{{ title }}</nav>
</template>
 
<style scoped>
nav {
  padding: 10px;
}
</style>
