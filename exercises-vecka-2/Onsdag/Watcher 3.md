Övning 2: Basic Watcher

ÖVNING: Text Counter
MÅL:

- Förstå hur watchers fungerar
- Reagera på förändringar i data

INSTRUKTIONER:

1. Skapa ett textfält där användaren kan skriva
2. Använd watch för att räkna antal ord i texten
3. Visa ordräkningen

// TextCounter.vue
<template>

  <div>
    <input type="text" v-model="text">
    <p>Antal ord: {{ wordCount }}</p>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

// Implementera din watcher här
</script>
