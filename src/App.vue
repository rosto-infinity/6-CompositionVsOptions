
<template>
  <div id="app">
    <h1>Compteur</h1>
    <p>Valeur actuelle : {{ count }}</p>
    <button @click="increment">Incrémenter</button>
    <button @click="decrement">Décrémenter</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0, // Valeur initiale du compteur
    };
  },
  methods: {
    increment() {
      this.count++; // Incrémente la valeur
    },
    decrement() {
      if (this.count > 0) {
        this.count--; // Décrémente la valeur si elle est supérieure à 0
      }
    },
  },
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
