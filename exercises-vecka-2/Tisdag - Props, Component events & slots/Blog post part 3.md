## Övning 3 - Sammankoppling (App)

### SCENARIOT:

Dags att koppla ihop allt i vår parent-komponent.

### MÅL:

- Förstå dataflödet mellan komponenter
- Hantera state i parent

### INSTRUKTIONER:

1. I App.vue:
   - Skapa state för ett post-objekt med title och body
   - Importera och använd båda komponenterna
   - Skicka rätt props till varje komponent
   - Uppdatera state när events tas emot

<script setup>
import { ref } from 'vue'
// Importera komponenter här
// Skapa state här
</script>
<template>
<div class="app">
<h1>Inlägg Förhandsgranskare</h1>
<!-- Implementera PreviewPost här -->
<!-- Implementera CreatePost här -->
</div>
</template>
<style scoped>
// Implementera styling här
</style>
