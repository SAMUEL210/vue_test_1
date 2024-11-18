<template>
  <p>Compteur : {{ count }}</p>
  <Button v-on:click="incrementer">incrementer</Button>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0)

const incrementer = () => {
  count.value++;
}
</script>

<style scoped>
p {
  color: red;
}
</style>
