<template>
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-semibold mb-2">Conseil du jour</h2>
    <p class="text-gray-700 italic">{{ tip }}</p>
    <button @click="nextTip" class="mt-2 bg-indigo-500 text-white px-4 py-2 rounded">Nouveau conseil</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const tips = [
  "Fais une pause pour respirer profondément.",
  "Écris 3 choses pour lesquelles tu es reconnaissant.",
  "Fais un geste gentil pour quelqu’un aujourd’hui.",
  "Visualise ton objectif de la semaine.",
  "Écoute une musique qui te fait du bien."
]
const tip = ref(tips[0])

function nextTip() {
  const index = Math.floor(Math.random() * tips.length)
  tip.value = tips[index]
}
</script>