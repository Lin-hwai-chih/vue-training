<script setup>
// console.log("我的第一個組件");
let message = "<u>Hello vue</u>";
let name = "content";
let checked = true;
let level = 0;
// let topics = ["HTML", "CSS", "JavaScript", "Vue.js"];
let topics = { html: "HTML", css: "CSS", js: "JavaScript", vue: "Vue.js" };
</script>

<template>
  <nav>基本的導覽列</nav>
  <!-- <main>練習樣板中的判斷式和迴圈</main> -->
  <main>
    <div v-if="level === 3">大神</div>
    <div v-else-if="level === 2">資深</div>
    <div v-else-if="level === 1">中階</div>
    <!-- <div v-else>入門</div> -->
    <div v-else>
      <div>入門</div>
      <ul>
        <!-- <li v-for="name in topics">{{ name }}</li> -->
        <!-- <li v-for="(name, index) in topics">{{ index }}-{{ name }}</li> -->
        <li v-for="(value, key) in topics">{{ key }}-{{ value }}</li>
      </ul>
    </div>
  </main>
  <!-- <main>基本的主內容</main> -->
  <!-- <main>{{ message }}</main> -->
  <!-- 標籤的內文 -->
  <!-- <main v-html="message"></main> -->
  <!-- <main v-html="message.toUpperCase()"></main> -->
  <!-- <main>{{ message.toUpperCase() }}</main> -->
  <!-- 標籤的屬性 -->
  <!-- <div v-bind:class="name">操作標籤的屬性</div> -->
  <!-- <div :class="name">操作標籤的屬性</div> -->
  <!-- <div :class="checked ? 'dark' : 'light'">操作標籤的屬性</div> -->
</template>
 
<style scoped>
main {
  background-color: #dddddd;
}
.content {
  color: blue;
}
.dark {
  color: #000;
}
.light {
  color: #888888;
}
</style>
