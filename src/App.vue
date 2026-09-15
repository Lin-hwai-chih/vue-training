<script setup>
let handle = function () {
  console.log("Click");
};

let mousemoveHandler = function () {
  console.log("Mouse Over");
};
</script>

<template>
  <nav>基本的導覽列</nav>

  <main>
    <!-- <button v-on:click="handle">按鈕</button> -->
    <!-- <button @click="handle" @mouseover="mousemoveHandler">按鈕</button> -->
    <button @click.once="handle" @mouseover="mousemoveHandler">按鈕</button>
    <!-- <a @click.prevent href="http://training.pada-x.com/">課程網站</a> -->
    <a @click.prevent="handle" href="http://training.pada-x.com/">課程網站</a>
  </main>
</template>
 
<style scoped>
main {
  background-color: #dddddd;
}
</style>
