<script setup>
import { ref } from "vue";

const className = ref("title");
</script>

<template>
  <h1 :class="className">Red title</h1>
</template>

<style scoped>
.title {
  color: red;
}
</style>