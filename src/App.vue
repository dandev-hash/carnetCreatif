<template>
  <div class="h-70 bg-gradient-to-l from-blue-100 to-purple-200 shadow-xl">
    <h1 class="text-8xl font-bold text-right pr-20 pt-15 text-purple-500 animate-bounce duration-1000">Carnet Créatif</h1>
    <p class="text-right text-2xl text-gray-500 pr-10 font-medium pt-5">Votre espace pour exprimer vos emotions et organiser votre journée.</p>
  </div>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-15 p-6">
    <EmotionForm />
    <Agenda />
    <DailyTip />
    <Notes />
    <Goals />
    <Wellness />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import EmotionForm from './components/EmotionForm.vue'
import Agenda from './components/Agenda.vue'
import DailyTip from './components/DailyTip.vue'
import Notes from './components/Notes.vue'
import Goals from './components/Goals.vue'
import Wellness from './components/Wellness.vue'
</script>