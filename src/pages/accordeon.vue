<script setup lang="ts">
import { ref } from 'vue';

const maVar = ref(false)
const maVar2 = ref(0)
</script>

<template>
  <p>la variable vaut : {{ maVar }}</p>
  <p>la variable2 vaut : {{ maVar2 }}</p><br><br>

  <button @click="maVar=false">Cacher</button><br>
  <button @click="maVar=true">Montrer</button><br>
  <button @click="maVar=!maVar">Bascule</button><br><br>

  <button @click="maVar2 = maVar2 === 1 ? 0 : 1">Montrer1</button>
  <h1 v-show="maVar2 === 1" class="text-2xl">Contenu1</h1>

  <h1 v-show="maVar" class="text-2xl">Bonjour monde, je suis GEOFFF ! </h1>
</template>
