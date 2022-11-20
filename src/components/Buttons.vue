<template>
  <div class="buttons">
    <button @click="storeCounter.decreaseCount">-</button>
    <button @click="storeCounter.increaseCount">+</button>
  </div>
</template>

<script>
import { useCounterStore } from "@/stores/counter";
export default {
  setup() {
    const storeCounter = useCounterStore();
    return {
      storeCounter,
    };
  },
};
</script>

<style>
</style>