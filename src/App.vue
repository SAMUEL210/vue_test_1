<template>
  <p>Compteur : {{ count }}</p>
  <Button v-on:click="incrementer">incrementer</Button>
  <Button v-on:click="decrementer">decrementer</Button>
  <ul>
    <li v-for="movie in Movies">{{ movie }}<Button @click="deleteMovie(movie)">Supprimer</Button></li>
  </ul>
</template>

<script setup>
import { ref } from "vue";

const Movies = ref(["Spider Man 2", "John Wick 1", "Avengers 1", "Avengers End Game", "John Wick 3"])
const count = ref(0)

const incrementer = () => {
  count.value++;
}
const decrementer = () => {
  count.value--;
}
const deleteMovie = (movie) => {
  Movies.value = Movies.value.filter((m) => m != movie )
}
</script>


<style scoped>
/* Scoped permet de limiter le CSS a cette page */

p {
  color: red;
}
</style>
