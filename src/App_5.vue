<script setup>
import { ref } from "vue";
let content = ref("");
let clearContent = function () {
  content.value = "";
};
let interests = ref([]);
// let color = ref(null);
let color = ref("");
</script>

<template>
  <nav>基本的導覽列</nav>

  <main>
    <!-- <h3>單選框</h3>
    紅色 <input type="radio" value="red" v-model="color" /> 綠色
    <input type="radio" value="green" v-model="color" />
    <div>使用者選擇的顏色：{{ color }}</div>
    <div :class="color">這是一段文字</div> -->

    <h3>多選框</h3>
    角色扮演
    <input type="checkbox" value="action" v-model="interests" /> 即時策略
    <input type="checkbox" value="rts" v-model="interests" /> 動作遊戲
    <input type="checkbox" value="RPG" v-model="interests" />
    <!-- <div>喜歡的遊戲類型：{{ interests }}</div> -->
    <div>喜歡的遊戲類型：</div>
    <ul>
      <li v-for="interest in interests">興趣：{{ interest }}</li>
    </ul>

    <h3>單行輸入框</h3>
    <input type="text" v-model="content" />
    <div>使用者輸入的文字是：{{ content }}</div>
    <button @click="clearContent">清空輸入框</button>

    <h3>下拉式選單</h3>
    <select v-model="color">
      <option value="">請選擇顏色</option>
      <option value="red">紅</option>
      <option value="green">綠</option>
    </select>
    <!-- <div>使用者選擇的顏色：{{ color }}</div> -->
    <div :class="color">這是一段文字</div>
  </main>
</template>
 
<style scoped>
.red {
  color: red;
}
.green {
  color: green;
}
main {
  background-color: #dddddd;
}
</style>
