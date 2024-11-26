Övning 1 - Simple Watcher
SCENARIOT: Vi ska skapa en enkel räknare som använder watchers för att reagera på ändringar.
MÅL: Förstå hur watchers fungerar
Se hur man kan övervaka reaktiv data
Lära sig watch syntax

INSTRUKTIONER:

1. Skapa en ny komponent WatcherDemo.vue:
<script setup>
import { ref, watch } from 'vue'

const count = ref(0)

// Implementera en watcher som loggar när count ändras
// watch(count, (newValue, oldValue) => {
// Implementera här
// })

</script>

<template>
  <div>
    <h2>Count: {{ count }}</h2>
    <button @click="count++">Öka</button>
    <button @click="count--">Minska</button>
  </div>
</template>

TIPS:

1. Använd console.log i watchern för att se både nya och gamla värdet
2. Testa olika sätt att ändra count
