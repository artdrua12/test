<script setup>
import TheBlock from "./components/TheBlock.vue";
import TheWelcome from "./components/TheWelcome.vue";
</script>

<template>
  <div class="app">
    <div class="menu">menu</div>
    <div class="header">header</div>
    <div class="main">
      <the-block v-for="(item, index) in 15" :key="index"></the-block>
    </div>
  </div>
</template>

<style scoped>
.app {
  display: grid;
  width: 100%;
  height: 100vh;
  grid-template-columns: 220px 1fr;
  grid-template-rows: 62px 1fr;
  background-color: #201379;
}

.menu {
  grid-area: 2/1/-1/2;
}

.header {
  grid-area: 1/1/-1/-1;
}
.main {
  grid-area: 2/2/-1/-1;
  background-color: #12094a;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  grid-template-rows: repeat(auto-fit, minmax(100px, 1fr));
  grid-gap: 10px;

  padding: 20px;
  overflow: hidden;
}
</style>
