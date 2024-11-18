<template>
  <p>Compteur : {{ count }}</p>
  <Button v-on:click="incrementer">incrementer</Button>
  <Button v-on:click="decrementer">decrementer</Button>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0)

const incrementer = () => {
  count.value++;
}
const decrementer = () => {
  count.value--;
}
</script>


<style scoped>
/* Scoped permet de limiter le CSS a cette page */

p {
  color: red;
}
</style>
