<template>
  <div class="child2">
    <h2>子组件2</h2>
    <h3>绑定多个v-model实现同步通信</h3>
    <button @click="handle1">btn-pageNo{{ pageNo }}</button> &nbsp;
    <button @click="$emit('update:pageSize',pageSize+10)">btn-pageSize{{ pageSize }}</button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(["pageNo", "pageSize"])
const $emit = defineEmits(["update:pageNo", "update:pageSize"])

const handle1 = () => {
  $emit("update:pageNo", props.pageNo + 2)
}


</script>

<style scoped>
.child2 {
  width: 600px;
  height: 300px;
  background: skyblue;
}
</style>
