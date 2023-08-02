<template>
  <div class="box">
    <h1>我是父亲组件</h1>
    <Child info="我是小明" :age="age"></Child>
  </div>
</template>

<script setup lang="ts">
import Child from './Child.vue'
import { ref } from "vue"

const age = ref(20)
</script>

<style scoped>
.box {
  width: 100vw;
  height: 400px;
  background: yellowgreen;
}
</style>
