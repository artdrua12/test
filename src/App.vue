<script setup>
import TheBlock from "./components/TheBlock.vue";
import TheMenuItem from "./components/TheMenuItem.vue";
import IconCommunity from "./components/icons/IconCommunity.vue";
</script>

<template>
  <div class="app">
    <div class="menu">
      <the-menu-item v-for="(item, index) in 7" :key="index"></the-menu-item>
    </div>
    <div class="header">
      <IconCommunity></IconCommunity>
      <span class="text"> Text</span>

      <button class="button enter">Вход</button>
      <button class="button registration">Регистрация</button>
    </div>
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
  overflow: hidden;
}

.menu {
  grid-area: 2/1/-1/2;
  background-color: #201379;
  display: flex;
  flex-direction: column;
  gap: 30px;
  padding: 20px;
}

.header {
  grid-area: 1/1/-1/-1;
  display: flex;
  align-content: center;
  padding: 20px;
  color: white;
  overflow: hidden;
  gap: 10px;
  height: 100%;
}

.text {
  margin-right: auto;
}

.button {
  width: 150px;
  height: 34px;
  border-radius: 4px;
  background-color: #201379;
  color: white;
}

.enter {
  border: 2px solid blue;
}

.registration {
  border: none;
  background: linear-gradient(0deg, blue, rgb(85, 0, 255));
}

.main {
  grid-area: 2/2/-1/-1;
  background-color: #0c0827;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  grid-template-rows: repeat(auto-fit, minmax(70px, 1fr));
  grid-gap: 10px;

  padding: 20px;
  overflow: hidden;
}
</style>
