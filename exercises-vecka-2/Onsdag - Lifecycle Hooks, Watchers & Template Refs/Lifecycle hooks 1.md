Övning 1 - Lifecycle Hooks Basics
SCENARIOT: Vi ska skapa en enkel komponent som demonstrerar de grundläggande lifecycle hooks.
MÅL: Förstå när olika lifecycle hooks triggas
Lära sig grundläggande syntax för hooks
Se hooks i action genom console.log

INSTRUKTIONER:

1. Skapa ett nytt Vue projekt med:
   npm create vue@latest
2. Skapa en ny komponent LifecycleDemo.vue:
<script setup>
import { onMounted, onBeforeMount, onUnmounted, ref } from 'vue'

const message = ref('Hello Vue!')

// Implementera hooks här som loggar till konsolen
// när komponenten går genom olika stadier

</script>

<template>
  <div>
    <h2>{{ message }}</h2>
    <button @click="message = 'Updated message!'">Uppdatera meddelande</button>
  </div>
</template>

3. Implementera följande hooks:
   onBeforeMount - logga "Komponenten förbereds"
   onMounted - logga "Komponenten är monterad"
   onUnmounted - logga "Komponenten är borttagen"

TIPS:

1. Använd App.vue för att villkorligt rendera LifecycleDemo med v-if
2. Kolla konsolen för att se när hooks triggas
3. Testa att toggla komponenten med en knapp
