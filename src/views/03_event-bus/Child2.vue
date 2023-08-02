<template>
  <div class="child2">
    <h2>我是子组件2:曹丕</h2>
    <button @click="handle">给我哥送把枪</button>
  </div>
</template>

<script setup lang="ts">
import $bus from "../../bus"
const handle = () => {
  $bus.emit("car", { car: "AK47" })
}
</script>

<style scoped>
.child2 {
  width: 300px;
  height: 300px;
  background: skyblue;
}
</style>
