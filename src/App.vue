<script setup>
import { ref } from 'vue'

const contador = ref(0)

function decrementar() {
  contador.value--
  if (contador.value < 0) {
  contador.value = 0;
}
}
function reset() {
  contador.value = 0;
}
</script>

<template>
  <div class="container">
  <button @click='contador++'>+</button>
  <p>{{ contador }}</p>
  <button @click="decrementar()">-</button>
  <button @click="reset()">C</button>
</div>
</template>

<style scoped>
  button {
    font-size: 2rem;
    padding: 1rem;
    margin: 1rem;
    cursor: pointer;
    border: none;
    background-color: rgb(255, 251, 199);
    border-radius: 0.5rem;
    transition: 300ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  button:hover {
    background-color: rgb(101, 136, 211);
  }
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  p {
    font-size: 2rem;
  }
</style>
