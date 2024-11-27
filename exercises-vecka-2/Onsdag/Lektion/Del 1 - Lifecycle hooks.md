SCENARIOT: Vi ska bygga en Movie Dashboard som visar användarens filmupplevelse från start till slut. Vi kommer använda olika lifecycle hooks för att hantera laddning, användarpreferenser och städning av data.

MÅL:

- Förstå när olika lifecycle hooks triggas
- Hantera laddningstillstånd och felhantering
- Spara och återställa användarens preferenser

INSTRUKTIONER:

1. Skapa MovieDashboard.vue:

<script setup>
import { ref, onMounted, onBeforeMount, onUnmounted } from 'vue'

const API_KEY = 'Ni får en nyckel av mig'

const getMovies = async (category) => {
  const res = await fetch(`http://www.omdbapi.com/?s=${category}&apikey=${API_KEY}`)
  return await res.json()
}

const movies = ref([])
const isLoading = ref(false)
const errorMessage = ref('')
const userPreferences = ref({
  category: 'action',  // Sparas/hämtas från localStorage
  darkMode: false     // Sparas/hämtas från localStorage
})

// 1. onBeforeMount
//    - Hämta användarens preferenser från localStorage
//    - Sätt upp grundläggande UI-state

// 2. onMounted
//    - Hämta filmer baserat på användarens kategori
//    - Hantera laddningstillstånd och fel
//    - Applicera dark mode om det var sparat

// 3. onUnmounted
//    - Spara användarens senaste preferenser
//    - Rensa eventuella error messages

</script>

<template>
  <div :class="{ 'dark-mode': userPreferences.darkMode }">
    <div class="header">
      <h1>Movie Dashboard</h1>
      <select v-model="userPreferences.category">
        <option value="action">Action</option>
        <option value="comedy">Comedy</option>
        <option value="drama">Drama</option>
      </select>
      <button @click="userPreferences.darkMode = !userPreferences.darkMode">
        Toggle Dark Mode
      </button>
    </div>

    <div v-if="errorMessage" class="error">
      {{ errorMessage }}
    </div>

    <div v-if="isLoading" class="loading">
      Laddar filmer...
    </div>

    <div v-else class="movie-grid">
      <!-- Movie cards här -->
    </div>

  </div>
</template>
