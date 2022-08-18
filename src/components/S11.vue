<script setup>
import { ref } from "vue";
import ChildComp from "./ChildComp4.vue";

const msg = ref("from parent");
</script>

<template>
  <ChildComp>Message: {{ msg }}</ChildComp>
</template>