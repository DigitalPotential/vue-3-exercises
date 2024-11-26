## Övning 2 - Props och Events (CreatePost)

### SCENARIOT:

Nu skapar vi CreatePost komponenten som låter användaren skriva både titel och innehåll.
När användaren skriver ska data skickas upp till parent genom events.

### MÅL:

- Förstå hur props skickar data från parent till child
- Lära sig hantera custom events
- Se hur komponenter kan kommunicera i båda riktningar
- Hantera multipla inputs och events

### INSTRUKTIONER:

1. Skapa en CreatePost komponent som:
   - Tar emot title och body som props
   - Emittar 'titleChanged' och 'bodyChanged' events
   - Har ett input-fält för titel
   - Har ett textarea för innehåll

### TIPS:

1. Använd `:value` för att binda props till inputs
2. Använd `@input` för att lyssna på ändringar
3. Skicka det nya värdet med emit: `emit('eventName', newValue)`
4. I parent, uppdatera state när events tas emot

<script setup>
// Definiera props för title och body
const props = defineProps({
// Implementera props här
})
// Definiera dina custom events
const emit = defineEmits([
// Lista dina events här
])
</script>
<template>
<div class="create-post">
<!-- Skapa input för titel som:
Använder title prop som value
Emittar titleChanged vid input -->
<input
type="text"
placeholder="Skriv din titel här..."
>
<!-- Skapa textarea för innehåll som:
Använder body prop som value
Emittar bodyChanged vid input -->
<textarea
placeholder="Skriv ditt inlägg här..."
></textarea>
</div>
</template>
<style scoped>
// Implementera styling här
</style>
