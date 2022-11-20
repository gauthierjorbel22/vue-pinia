<template>
  <div class="about">
    <h1>About</h1>
    <button @click="storeCounter.increaseCount" class="counter-button">{{ storeCounter.count }}</button>
  </div>
</template>

<script>
import { useCounterStore } from "../stores/counter";
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
.counter-button {
  font-size: 50px;
}
</style>
  