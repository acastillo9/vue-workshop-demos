<script setup>
import { ref, computed } from "vue";
import S1 from "./components/S1.vue";

const routes = {
  "/s1": S1,
};

const currentPath = ref(window.location.hash);

window.addEventListener("hashchange", () => {
  currentPath.value = window.location.hash;
});

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || "/"] || S1;
});
</script>

<template>
  <component :is="currentView" />
</template>
