<script setup lang="ts">
import { ref } from 'vue'

const clicked = ref(false)
const buttonClass = ref('bluebutton')
function whenclicked() {
  clicked.value = !clicked.value
}
</script>

<template>
  <button :class="buttonClass" @click="whenclicked">button</button>
  <p>{{ clicked }}</p>
</template>

<style scoped>
.bluebutton {
  background-color: #3b3f7a;
  color: #eef7f9;
  border: none;
  border-radius:8px;
  padding: 10px 20px;
}
.bluebutton:active {
  background-color: #eef7f9;
  color: #3b3f7a;
}
</style>
