<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<template>
  <p>count is: {{ count }}</p>
  <button @click="increment">+1</button>
</template>
