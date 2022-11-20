<template>
  <div class="home">
    <Counter />
    <Buttons />
    <hr />
    <div>This counter is: {{ storeCounter.oddOrEven }}</div>
    <hr />
    <div>
      <h3>Edit counter:</h3>
      <input type="number" v-model="storeCounter.count" />
    </div>
  </div>
</template>
<script>
import { useCounterStore } from "@/stores/counter";
import Counter from "../components/Counter.vue";
import Buttons from "../components/Buttons.vue";
export default {
  components: {
    Counter,
    Buttons,
  },
  setup() {
    const storeCounter = useCounterStore();
    return {
      storeCounter,
    };
  },
};
</script>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}
.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
