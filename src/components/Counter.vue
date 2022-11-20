<template>
    <div class="count">
      {{ storeCounter.count }}
    </div>
</template>

<script>
import { useCounterStore } from "@/stores/counter";
export default {
setup(){
    const storeCounter = useCounterStore();
    return {
        storeCounter
    }
}
}
</script>

<style>

</style>