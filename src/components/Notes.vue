<template>
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-semibold mb-2">Notes libres</h2>
    <textarea v-model="note" class="w-full p-2 border rounded" rows="4" placeholder="Note tes idées, inspirations..."></textarea>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const note = ref('')
</script>