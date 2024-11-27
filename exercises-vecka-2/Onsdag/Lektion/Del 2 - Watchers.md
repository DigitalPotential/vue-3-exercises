SCENARIOT: Nu ska vi göra vår Movie Dashboard "smartare" genom att implementera reaktiv filmfiltrering, sökhistorik och användarstatistik.

MÅL:

- Förstå hur watchers kan användas för att reagera på ändringar
- Implementera smart sökfiltrering
- Spara användaraktivitet och statistik

INSTRUKTIONER:

1. Utöka MovieDashboard.vue med följande funktionalitet:

<script setup>
// ... tidigare kod ...

// Ny state för sökning och statistik
const searchQuery = ref('')
const filteredMovies = ref([])
const searchHistory = ref([])
const viewStats = ref({
  totalSearches: 0,
  mostSearchedGenre: '',
  viewedMovies: new Set()
})

// 1. Watch searchQuery
// - Filtrera movies baserat på titel
// - Spara sökningen i searchHistory om den gav resultat
// - Uppdatera totalSearches i viewStats

// 2. Watch userPreferences.category
// - Hämta nya filmer när kategorin ändras
// - Uppdatera mostSearchedGenre i viewStats
// - Nollställ searchQuery

// 3. Watch filteredMovies
// - Uppdatera UI med antalet hittade filmer
// - Logga om inga filmer hittades

// Extra: Deep watch på viewStats för att spara till localStorage
</script>

<template>
  <div :class="{ 'dark-mode': userPreferences.darkMode }">
    <!-- Tidigare template kod... -->
    
    <div class="search-section">
      <input 
        v-model="searchQuery"
        type="text" 
        placeholder="Sök bland filmer..."
      >
      <div class="search-history">
        <h3>Senaste sökningar:</h3>
        <ul>
          <li v-for="search in searchHistory.slice(-5)" :key="search">
            {{ search }}
          </li>
        </ul>
      </div>
    </div>

    <div class="stats">
      <p>Antal sökningar: {{ viewStats.totalSearches }}</p>
      <p>Mest sökta genre: {{ viewStats.mostSearchedGenre }}</p>
    </div>

    <div class="movie-grid">
      <!-- Visa filteredMovies istället för movies -->
    </div>

  </div>
</template>
