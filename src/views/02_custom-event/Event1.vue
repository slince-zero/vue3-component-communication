<template>
  <div class="son">
    <p>我是子组件1</p>
    <button @click="handle">点我触发自定义事件</button>
  </div>
</template>

<script setup lang="ts">
// 接收父组件传过来的自定义事件
let emit = defineEmits(["xxx"])
const handle = () => {
  emit("xxx", "小明", "18")
}
</script>

<style scoped>
.son {
  width: 400px;
  height: 200px;
  background: skyblue;
}
</style>
