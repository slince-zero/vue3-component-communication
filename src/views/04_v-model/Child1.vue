<template>
  <div class="child1">
    <h2>子组件1</h2>
    <h3>老爹给的money:{{ money }}</h3>

    <button @click="handle">实现我跟老爹金钱数目相同</button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(["money"])
const emit = defineEmits(["updateMoney"])
const handle = () => {
  emit("updateMoney", props.money + 1000)
}
</script>

<style scoped>
.child1 {
  width: 300px;
  height: 300px;
  background: hotpink;
}
</style>
