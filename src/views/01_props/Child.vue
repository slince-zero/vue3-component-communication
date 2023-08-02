<template>
  <div class="son">
    <h1>我是儿子组件</h1>
    <h2>姓名：{{ info }}</h2>
    <h2>年龄：{{ age }}</h2>
  </div>
</template>

<script setup lang="ts">
const propsArr = defineProps(["info", "age"])
console.log(propsArr);

</script>

<style scoped>
.son {
  width: 400px;
  height: 200px;
  background: hotpink;
}
</style>
