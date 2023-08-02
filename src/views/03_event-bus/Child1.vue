<template>
  <div class="child1">
    <h3>我是子组件1:曹植</h3>
  </div>
</template>

<script setup lang="ts">
import $bus from "../../bus"
import { onMounted } from "vue"
onMounted(() => {
  $bus.on("car", (car) => {
    console.log(car)
  })
})
</script>

<style scoped>
.child1 {
  width: 300px;
  height: 300px;
  background: hotpink;
}
</style>
