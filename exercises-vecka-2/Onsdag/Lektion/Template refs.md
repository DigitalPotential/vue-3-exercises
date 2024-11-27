SCENARIOT: Vi ska göra vår Movie Dashboard mer användarvänlig genom att implementera smart keyboard navigation och fokushantering.

MÅL:

- Förstå hur template refs kan användas för DOM-manipulation
- Implementera keyboard shortcuts för snabb navigation
- Hantera fokus mellan sökfält och filmkort

INSTRUKTIONER:

1. Utöka MovieDashboard.vue med följande:

<script setup>
import { ref, onMounted } from 'vue'

// Skapa dessa refs:
const searchInput = ref(null)
const movieCards = ref([])
const currentFocusIndex = ref(-1)

// Vi ger grundstrukturen - du implementerar logiken:
const handleKeyboardNavigation = (e) => {
  if (e.key === '/') {
    // Implementera: 
    // - Fokusera sökfältet
    // - Förhindra att '/' skrivs i input
  }
  
  if (e.key === 'ArrowDown' || e.key === 'ArrowUp') {
    // Implementera:
    // - Uppdatera currentFocusIndex beroende på piltangent
    // - Fokusera rätt filmkort
    // - Se till att inte gå utanför array-gränserna
  }
}

// Implementera:
// - onMounted för att sätta initialt fokus på sökfältet

</script>

<template>
  <div @keydown="handleKeyboardNavigation">
    <!-- 
      Implementera:
      - Lägg till ref för sökfältet
    -->
    <input 
      v-model="searchQuery"
      type="text" 
      placeholder="Tryck '/' för att söka..."
    >

    <!--
      Implementera:
      - Bind varje filmkort till movieCards array med :ref
      - Gör korten fokuserbara med tabindex
      - Lägg till styling för fokuserat kort
    -->
    <div class="movie-grid">
      <div
        v-for="(movie, index) in filteredMovies"
        :key="movie.imdbID"
      >
        <h3>{{ movie.Title }}</h3>
        <p>{{ movie.Year }}</p>
      </div>
    </div>

  </div>
</template>

TIPS:

1. Använd element.focus() för att fokusera ett element
2. Kom ihåg e.preventDefault() för att hindra default beteenden
3. För att binda ref till en array av element:
   :ref="el => movieCards[index] = el"
4. Använd :tabindex="0" för att göra element fokuserbara
