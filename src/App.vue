<template>
  <div id="app">
    <button @click.prevent="submit">Submit</button>
    <BaseAxios
      v-if="isAxios"
      methods="get"
      url="https://jsonplaceholder.typicode.com/todos/1"
      title="All Todos"
      name="todos"
    />
  </div>
</template>

<script setup>
import BaseAxios from './components/BaseAxios.vue'
import { ref } from 'vue'
const isAxios = ref(false)

function submit() {
  isAxios.value = true
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
