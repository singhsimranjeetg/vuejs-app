<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/HelloWorld.vue';
import { ref } from 'vue';

const quantity = ref(0);
const msgVar = 'Hello Simranjeet Singh';
function increment() {
  quantity.value++;
}
function decrement() {
  quantity.value--;
  if (quantity.value < 0) {
    quantity.value = 0;
  }
}
</script>

<template>
  <div>
    <HelloWorld :msg="msgVar" />
    <div class="qty__selector">
      <button @click="increment">+</button>
      <span>{{ quantity }}</span>
      <button @click="decrement">-</button>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  border: none;
  background: transparent;
  cursor: pointer;
}
.qty__selector {
  border: 1px solid #eee;
  max-width: 70px;
  border-radius: 5px;
  background-color: #f3f3f3;
}
.qty__selector span {
  margin: 0 5px;
}
</style>
