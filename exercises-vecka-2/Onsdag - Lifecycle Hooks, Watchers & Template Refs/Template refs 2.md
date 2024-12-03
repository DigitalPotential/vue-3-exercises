Övning 2 - Multi Input Navigation
SCENARIOT: Vi ska skapa en komponent med tre input-fält där användaren automatiskt flyttas till nästa fält när Enter trycks. Detta är ett vanligt mönster i t.ex. verifieringskoder.
MÅL: Hantera flera template refs samtidigt
Implementera keyboard navigation
Förstå dynamisk ref-binding
INSTRUKTIONER:

1. Skapa en ny komponent AdvancedInputDemo.vue:
<script setup>
import { ref, onMounted } from 'vue'

// Skapa en array för att lagra referenser till input-elementen
const inputs = ref([])
// Håll reda på vilket input-fält som är aktivt
const currentIndex = ref(0)

// Implementera en funktion som flyttar fokus till nästa input

// Fokusera första input-fältet när komponenten monteras

</script>

<template>
  <div class="input-demo">
    <!-- Skapa tre input-fält med v-for -->
    <!-- Bind varje input till inputs-arrayen med :ref -->
    <!-- Lägg till event handler för Enter-tangenten -->
  </div>
</template>

TIPS:

1. Använd v-for="(\_, index) in 3" för att skapa input-fälten
2. Bind ref med :ref="el => inputs[index] = el"
3. Använd @keyup.enter för att lyssna efter Enter-tangenten
4. Kontrollera att currentIndex inte går utanför inputs-arrayens längd
