<template>
  <div id="app">
    <h1>Compteur</h1>
    <p>Valeur actuelle : {{ count }}</p>
    <button @click="increment">Incrémenter</button>
    <button @click="decrement">Décrémenter</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0); // Valeur initiale du compteur

const increment = () => {
  count.value++; // Incrémente la valeur
};

const decrement = () => {
  if (count.value > 0) {
    count.value--; // Décrémente la valeur si elle est supérieure à 0
  }
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 50px;
}

button {
  margin: 5px;
  padding: 10px 20px;
}
</style>
