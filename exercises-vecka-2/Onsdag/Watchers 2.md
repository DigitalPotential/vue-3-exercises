Övning - Form Validation med Watchers
SCENARIOT: Vi ska skapa ett enkelt formulär som validerar email och lösenord i realtid med hjälp av watchers. Detta är ett vanligt användningsfall för att ge användaren direkt feedback.
MÅL: Förstå hur watchers fungerar
Implementera realtidsvalidering
Hantera flera watchers samtidigt
Lära sig uppdatera error states

INSTRUKTIONER:

1. Skapa en ny komponent FormWatcherDemo.vue:
<script setup>
import { ref, watch } from 'vue'

// Skapa refs för email, password och errors
const email = ref('')
const password = ref('')
const errors = ref({})

// Implementera en watcher för email som validerar:
// - Måste innehålla @
// - Ta bort error om valid

// Implementera en watcher för password som validerar:
// - Minst 6 tecken
// - Ta bort error om valid

</script>

<template>
  <div class="form-demo">
    <!-- Skapa input för email med error-meddelande -->
    <!-- Skapa input för password med error-meddelande -->
  </div>
</template>

TIPS:

1. Använd watch(email, (newValue) => { }) för att övervaka ändringar
2. Lagra errors i ett objekt: errors.value.email = 'Felmeddelande'
3. Ta bort error med delete errors.value.email
4. Använd v-if för att visa felmeddelanden
