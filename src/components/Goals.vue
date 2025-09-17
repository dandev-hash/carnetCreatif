<template>
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-semibold mb-2">Objectifs personnels</h2>
    <input v-model="goal" class="border p-2 rounded w-full mb-2" placeholder="Définis un objectif" />
    <button @click="addGoal" class="bg-indigo-500 text-white px-4 py-2 rounded">Ajouter</button>
    <ul class="mt-4 list-disc pl-5">
      <li v-for="(g, i) in goals" :key="i">{{ g }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const goal = ref('')
const goals = ref([])

function addGoal() {
  if (goal.value.trim()) {
    goals.value.push(goal.value)
    goal.value = ''
  }
}
</script>