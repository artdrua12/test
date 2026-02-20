<script setup>
import DocumentationIcon from "./icons/IconDocumentation.vue";
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="block">
    <div class="img"></div>

    <div class="bottom">
      <span>Game Olympic</span>
      <DocumentationIcon />
    </div>
  </div>
</template>

<style scoped>
.block {
  display: flex;
  flex-direction: column;
  border-radius: 15px;
  overflow: hidden;
}

.img {
  grid-area: 1/1/2/-1;
  background-image: url('../assets/images.jpg');
  background-size: cover;
  background-position: center center;
  height: 100%;
}

.bottom {
  background: red;
  display: flex;
  justify-content: space-between;
  padding:5px 10px;
  color: azure;
}
</style>
