<script setup>
import { ref, computed } from "vue";
import S1 from "./components/S1.vue";
import S2 from "./components/S2.vue";
import S3 from "./components/S3.vue";
import S4 from "./components/S4.vue";
import S5 from "./components/S5.vue";
import S6 from "./components/S6.vue";
import S7 from "./components/S7.vue";
import S8 from "./components/S8.vue";
import S9 from "./components/S9.vue";
import S10 from "./components/S10.vue";
import S11 from "./components/S11.vue";

const routes = {
  "/s1": S1,
  "/s2": S2,
  "/s3": S3,
  "/s4": S4,
  "/s5": S5,
  "/s6": S6,
  "/s7": S7,
  "/s8": S8,
  "/s9": S9,
  "/s10": S10,
  "/s11": S11,
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
