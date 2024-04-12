<script setup lang="ts">
import { ref } from 'vue';

const sectionOpen = ref(false)
const sectionOpen2 = ref(0)
const sectionsData = [
  {
    label: 'bouton 1',
    texte: `texte panneau 1 Lorem ipsum dolor sit ame
    consectetur adipisicing elit. Inventore animi dolore,
    rerum magni laudantium quod excepturi laboriosam, 
    ex modi debitis harum reprehenderit eaque quam ut
    ea molestiae. Id, cum dolor!`
  },
  {
    label: 'bouton 2',
    texte: `texte panneau 2 Amet alias provident quos quis, 
    Officia ut ab dolores quos dolorem accusamus ad,
    consectetur unde minima, ipsum eligendi inventore id
    labore, laborum rerum laboriosam corrupti iste.
    Distinctio, perspiciatis!`
  },
  {
    label: 'bouton 3',
    texte: `texte panneau 3 Repudiandae corporis voluptates, 
    odit reprehenderit sint pariatur at voluptatum, cumque
    quia sit eligendi ex culpa eos, alias magnam molestiae
    id modi accusantium ipsa eveniet accusamus. Tempora 
    quis corporis et nam.`
  }
]

</script>

<template>

  <div class="border">
    <p>la variable vaut : {{ sectionOpen }}</p>
    <p>la variable2 vaut : {{ sectionOpen2 }}</p><br><br>

    <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 mx-3"
      @click="sectionOpen = false">Cacher</button><br>
    <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 mx-3"
      @click="sectionOpen = true">Montrer</button>
    <button class="rounded-full border-2 border-green-600 bg-green-300 px-2 m-3"
      @click="sectionOpen = !sectionOpen">Bascule</button>

    <h1 v-show="sectionOpen" class="text-2xl">Bonjour monde, je suis GEOFFF ! </h1><br><br>

    <!-- <button class="rounded-full border-2 border-red-600 bg-red-300 px-2 mx-3 m-3"
      @click="sectionOpen2 = sectionOpen2 === 1 ? 0 : 1">Montrer1</button>
    <h1 v-show="sectionOpen2 === 1" class="text-2xl">Contenu1</h1> -->
  </div>

  <div class="border my-10">
    <section v-for="({ label, texte }, key) of sectionsData" :key="key">
      <pre class="font-mono">key : {{ key }}</pre>
      <button @click="sectionOpen2 = sectionOpen2 === key ? -1 : key"
        class="font-mono rounded-full border-2 border-green-600 bg-green-300 px-2 m-3">label : {{ label }}</button>
      <p v-show="sectionOpen2 === key" class="font-mono">texte : {{ texte }}</p>
    </section>
  </div>


</template>
