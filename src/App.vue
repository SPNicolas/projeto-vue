<script setup>
import { ref } from 'vue';

const nome = 'Nicolas';
const idd = 15;
const contador = ref(0);

function inverter(texto) {
  return texto.split('').reverse().join('')
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  }
}
function resetar() {
  contador.value = 0
}




</script>

<template>
  <div class="info">
    <h1>Informações</h1>
    <p>Nome: {{ nome }}</p>
    <p>Idade: {{ idd }}</p>
    <p>Nome invertido: {{ inverter(nome).toUpperCase() }}</p>
  </div>
  <div class="button"> 
  <button class="botao" @click="contador++">+</button>
  <button class="botao" @click="decrementar">-</button>
  <button class="botao" @click="resetar">zerar</button>
  <p>Valor do contador: {{ contador }}</p></div>
 
  <div v-if="contador > 10" class="azul">
    <p>Já passou de 10</p>
  </div>
  <div v-else class="vermelho">
    <p>Não passou de 10</p>
  </div>
</template>

<style scoped>
button {
  background-color: black;
  color: aliceblue;


}

.azul {
  background-color: blue;
  color: white;
}

.vermelho {
  background-color: red;
  color: white;
}

.info {
  background-color: rgba(35,12,22,1);
  padding: 70px 80px;
  color: rgb(183, 210, 219);
  border-radius: 10px;

}
</style>
