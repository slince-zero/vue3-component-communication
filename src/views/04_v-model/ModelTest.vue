<template>
  <div class="father">
    <h1>父组件</h1>
    <h2>我给了儿子1：{{ money }}</h2>
    <h2>儿子2同步过来的数据:{{ pageNo }}---{{ pageSize }}</h2>
    <div class="container">
      <Child1 :money="money" @updateMoney="handle"></Child1>
      <Child2 v-model:pageNo="pageNo" v-model:pageSize="pageSize"></Child2>
    </div>
  </div>
</template>

<script setup lang="ts">
import Child1 from "./Child1.vue"
import Child2 from "./Child2.vue"
import { ref } from "vue"

let money = ref(1000)

const handle = (num: number) => {
  money.value = num
}

const pageNo = ref(3)
const pageSize = ref(10)
</script>

<style scoped>
.father {
  background: gray;
}
.container {
  display: flex;
  justify-content: space-between;
}
</style>
