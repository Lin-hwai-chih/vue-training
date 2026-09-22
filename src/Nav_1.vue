<script setup>
defineProps(["title", "subtitle"]);
</script>

<template>
  <!-- <nav>基本的導覽列</nav> -->
  <!-- <nav>{{ title }}</nav> -->
  <nav>
    <div>{{ title }}</div>
    <div>{{ subtitle }}</div>
  </nav>
</template>
 
<style scoped>
nav {
  padding: 10px;
}
</style>
