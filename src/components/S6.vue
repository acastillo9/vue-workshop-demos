<script setup>
import { ref } from "vue";

const clientes = ref([
  { id: 1, nombre: "Juan" },
  { id: 2, nombre: "Carlos" },
  { id: 3, nombre: "Luis" },
]);
</script>

<template>
  <ul>
    <li v-for="cliente in clientes" :key="cliente.id">
      {{ cliente.nombre }}
    </li>
  </ul>
</template>