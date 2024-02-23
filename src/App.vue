<script setup>
import { ref } from 'vue';

const contador = ref(0);

function decrementar() {
  contador.value--
}
function resetar() {
  contador.value = 0
}

if (contador < 0) {
  
}
</script>

<template>
  <button @click="contador++">+</button>
  <button @click="decrementar">-</button>
  <button @click="resetar">zerar</button>
  <p>Valor do contador: {{  contador }}</p>
</template>

<style scoped>
button{
  background-color: black;
  color: aliceblue;
  margin: 5pxe;
  width: 100px;
}
</style>
