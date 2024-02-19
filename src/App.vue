<script setup>
import { ref } from 'vue';

const contador = ref(0);

const pessoa = {
  nome: 'Nicolas',
  cidade: 'Joinville'
};

pessoa.nome = 'Novo nome';
</script>

<template>
  <button @click="contador++">+</button>
  <button @click="contador--">-</button>
  <p>Valor do contador: {{  contador }}</p>
</template>

<style scoped>

</style>
