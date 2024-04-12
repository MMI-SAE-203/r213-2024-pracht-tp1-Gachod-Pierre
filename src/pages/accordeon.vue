<script setup lang="ts">
import { ref } from 'vue';

const sectionOpen = ref(false)
const sectionOpen2 = ref(0)
</script>

<template>
  <p>la variable vaut : {{ sectionOpen }}</p>
  <p>la variable2 vaut : {{ sectionOpen2 }}</p><br><br>

  <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 mx-3"
    @click="sectionOpen=false">Cacher</button><br>
  <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 mx-3"
    @click="sectionOpen=true">Montrer</button>
  <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 m-3"
    @click="sectionOpen=!sectionOpen">Bascule</button>

  <h1 v-show="sectionOpen" class="text-2xl">Bonjour monde, je suis GEOFFF ! </h1><br><br>

  <button class="rounded-full border-2 border-red-600 bg-red-300 px-2 mx-3 m-3"
    @click="sectionOpen2 = sectionOpen2 === 1 ? 0 : 1">Montrer1</button>
  <h1 v-show="sectionOpen2 === 1" class="text-2xl">Contenu1</h1>

</template>
