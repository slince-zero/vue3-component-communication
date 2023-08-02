<template>
  <div class="child1">
    <h1>孙子组件</h1>
    <p>{{ car }}</p>
    <button @click="change">变化</button>
  </div>
</template>

<script setup lang="ts">
import { inject } from "vue"
let car:any =  inject("TOKEN")
console.log(car);

const change =()=>{
  car.value = '自行车'
}
</script>

<style scoped>
.child1 {
  width: 200px;
  height: 200px;
  background: red;
}
</style>
