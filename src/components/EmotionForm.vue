<template>
  <div class="bg-nude p-6 rounded-xl shadow border-0 ">
    <h2 class="text-2xl font-semibold text-pastel-text mb-4">Exprime ton ressenti</h2>
    <textarea
      v-model="emotion"
      class="w-full p-3 border border-pastel-gray rounded-lg bg-white text-pastel-text"
      rows="4"
      placeholder="Comment te sens-tu aujourd'hui ?"
    ></textarea>
    <button
      @click="save"
      class="mt-4 bg-pastel-accent text-purple-400 px-4 py-2  rounded-lg hover:bg-purple-100 transition"
    >
      Enregistrer
    </button>
    <p v-if="saved" class="text-green-600 mt-2">Émotion enregistrée ✅</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const emotion = ref('')
const saved = ref(false)

function save() {
  if (emotion.value.trim()) {
    saved.value = true
    setTimeout(() => (saved.value = false), 2000)
  }
}
</script>