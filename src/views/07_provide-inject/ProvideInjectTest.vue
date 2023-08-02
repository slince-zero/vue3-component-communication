<template>
  <div class="box">
    <h1>Provide与Inject{{car}}</h1>
    <hr />
    <Child></Child>
  </div>
</template>

<script setup lang="ts">
import Child from "./Child.vue";
//vue3提供provide(提供)与inject(注入),可以实现隔辈组件传递数据
import { ref, provide } from "vue";
let car = ref("法拉利");

// 两个参数，第一个个数据key，第二个是值value
provide("TOKEN", car);
</script>

<style scoped>
.box {
  width: 100vw;
  height: 600px;
  background: skyblue;
}
</style>