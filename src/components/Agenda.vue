<template>
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-semibold mb-2">Agenda du jour</h2>
    <input v-model="task" class="border p-2 rounded w-full mb-2" placeholder="Ajouter une tâche" />
    <button @click="addTask" class="bg-indigo-500 text-white px-4 py-2 rounded">Ajouter</button>
    <ul class="mt-4 list-disc pl-5">
      <li v-for="(t, i) in tasks" :key="i">{{ t }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const task = ref('')
const tasks = ref([])

function addTask() {
  if (task.value.trim()) {
    tasks.value.push(task.value)
    task.value = ''
  }
}
</script>