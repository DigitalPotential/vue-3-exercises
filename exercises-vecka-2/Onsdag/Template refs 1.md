Övning 1 - Template Refs Basic
SCENARIOT: Vi ska skapa en enkel input-komponent som använder template refs för att fokusera input-fältet.
MÅL: Förstå hur template refs fungerar
Lära sig manipulera DOM-element direkt
Se skillnad på reaktiv ref och template ref

INSTRUKTIONER:

1. Skapa en ny komponent TemplateRefDemo.vue:
<script setup>
import { ref, onMounted } from 'vue'

const inputRef = ref(null)

// Använd onMounted för att fokusera input-fältet
// när komponenten har monterats

</script>

<template>
  <div>
    <input 
      ref="inputRef"
      type="text" 
      placeholder="Detta fält ska fokuseras automatiskt"
    >
  </div>
</template>

TIPS:

1. Använd inputRef.value.focus() i onMounted
2. Testa att lägga till en knapp som fokuserar input-fältet
