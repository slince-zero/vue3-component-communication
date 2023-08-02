<template>
  <div>
    <h1>事件</h1>
    <Event1 @xxx="handle"></Event1>
  </div>
</template>

<script setup lang="ts">
import Event1 from "./Event1.vue"

const handle = (param1:string, param2:string) => {
  console.log(param1,param2);
  
}
</script>

<style scoped></style>
