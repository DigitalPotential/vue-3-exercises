// === Dag 3: Övning 1 - v-for ===
/\*
ÖVNING: Lista med v-for
MÅL:

- Förstå och använda v-for direktivet
- Hantera listor och objekt med v-for
- Använda key med v-for

INSTRUKTIONER:

1.  Skapa en lista med enkla strängar
2.  Skapa en lista med objekt
3.  Använd v-for med index
    \*/
    <template>
      <div class="lists">
        <!-- Lista med strängar -->
        <ul>
          <!-- Implementera v-for här -->
        </ul>

        <!-- Lista med objekt -->
        <div class="cards">
          <!-- Implementera v-for med objekt här -->
        </div>

      </div>
    </template>

<script setup>
// Skapa arrays för v-for här
const simpleList = ['Äpple', 'Banan', 'Citron']
const objectList = [
  { id: 1, name: 'Produkt 1', price: 99 },
  { id: 2, name: 'Produkt 2', price: 149 },
  { id: 3, name: 'Produkt 3', price: 199 }
]
</script>

// === Dag 3: Övning 2 - Data Fetching ===
/\*
ÖVNING: API Anrop
MÅL:

- Förstå asynkrona anrop i Vue
- Hantera loading states
- Visa hämtad data

INSTRUKTIONER:

1.  Skapa en komponent som hämtar data
2.  Implementera loading state
3.  Visa datan när den är hämtad
    \*/
    <template>
      <div class="data-fetching">
        <!-- Implementera loading state -->
        <div v-if="loading">
          Laddar...
        </div>

        <!-- Visa data -->
        <div v-else>
          <!-- Visa hämtad data här -->
        </div>

      </div>
    </template>

<script setup>
import { ref, onMounted } from 'vue'

const data = ref(null)
const loading = ref(false)

// Implementera fetchData funktion här
</script>

// === Dag 3: Övning 3 - Composables ===
/\*
ÖVNING: Enkel Composable
MÅL:

- Förstå grunderna i composables
- Skapa en återanvändbar funktion
- Använda composable i en komponent

INSTRUKTIONER:

1. Skapa en enkel counter composable
2. Använd composable i en komponent
3. Visa hur man delar state mellan komponenter
   \*/

// useCounter.js
import { ref } from 'vue'

export function useCounter(initialValue = 0) {
// Implementera counter logik här
}

// CounterComponent.vue
<template>

  <div class="counter">
    <!-- Använd counter composable här -->
  </div>
</template>

<script setup>
import { useCounter } from './composables/useCounter'
// Använd composable här
</script>
