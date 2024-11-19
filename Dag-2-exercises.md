// === Dag 2: Övning 1 - Styling ===
/\*
ÖVNING: Stilad Komponent
MÅL:

- Förstå olika sätt att stila i Vue
- Använda class och style bindings
- Prova inline styles

INSTRUKTIONER:

1.  Skapa en komponent med olika styling-metoder
2.  Använd både statiska och dynamiska klasser
3.  Testa inline styling
    \*/
    <template>
      <div class="styled-component">
        <!-- Prova olika styling metoder här -->
        <div class="static-class" :class="dynamicClass">
          Statisk och dynamisk klass
        </div>

        <div :style="{ color: textColor, fontSize: fontSize + 'px' }">
          Inline styling
        </div>

      </div>
    </template>

<script setup>
const dynamicClass = 'active'
const textColor = 'blue'
const fontSize = 16
</script>

<style>
.static-class {
  padding: 10px;
}
.active {
  background-color: #e0e0e0;
}
</style>

// === Dag 2: Övning 2 - Reactivity Basics & ref() ===
/\*
ÖVNING: Reaktiv Räknare
MÅL:

- Förstå reaktivitet i Vue
- Använda ref() för reaktiva variabler
- Se hur reaktiva uppdateringar fungerar

INSTRUKTIONER:

1. Skapa en enkel räknare med ref()
2. Lägg till knappar för att ändra värdet
3. Visa hur värdet uppdateras i realtid
\*/
<template>
  <div class="counter">
    <!-- Implementera räknare här -->
    <p>Nuvarande värde: <!-- Visa reaktivt värde här --></p>
    
    <!-- Lägg till knappar här -->
  </div>
</template>

<script setup>
import { ref } from 'vue'
// Skapa din reaktiva variabel här
</script>

// === Dag 2: Övning 3 - Computed & Conditional ===
/\*
ÖVNING: Status Checker
MÅL:

- Använda computed properties
- Implementera villkorlig rendering
- Kombinera reaktivitet med villkor

INSTRUKTIONER:

1.  Skapa ett formulär med ett inputfält för ett nummer
2.  Använd computed för att beräkna om numret är:
    - Positivt/Negativt
    - Jämnt/Udda
3.  Visa olika meddelanden baserat på computed values
    \*/
    <template>
      <div class="status-checker">
        <!-- Lägg till input här -->
        <input type="number" v-model="number">

        <!-- Använd v-if/v-else för att visa olika meddelanden -->
        <div v-if="isPositive">
          <!-- Positiv/Negativ status här -->
        </div>

        <div v-if="isEven">
          <!-- Jämn/Udda status här -->
        </div>

      </div>
    </template>

<script setup>
import { ref, computed } from 'vue'

const number = ref(0)

// Skapa dina computed properties här
</script>
