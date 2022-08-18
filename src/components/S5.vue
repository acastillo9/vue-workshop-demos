<script setup>
import { ref } from "vue";

const hiddenMessage = ref(true);

function toggleMessage() {
  hiddenMessage.value = !hiddenMessage.value;
}
</script>

<template>
  <button @click="toggleMessage">
    {{ hiddenMessage ? "mostrar mensaje oculto" : "ocultar mensaje" }}
  </button>
  <h1 v-if="hiddenMessage">para ver el mensaje oculto presiona el botón</h1>
  <h1 v-else>Vue es increible! 👽</h1>
</template>

