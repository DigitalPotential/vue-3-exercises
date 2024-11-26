# Vue 3 Komponentsövningar - Blog Post Creator

## Övning 1 - Basic Props (PreviewPost)

### SCENARIOT:

Vi ska bygga en blog post förhandsgranskare!
Först skapar vi en PreviewPost komponent som visar både titel och innehåll som den får från parent.

### MÅL:

- Förstå hur props skickar data från parent till child
- Lära sig props validation
- Hantera multipla props

### INSTRUKTIONER:

1. Skapa en PreviewPost komponent som tar emot:
   - title (required, string)
   - body (required, string)
2. Visa titel i en h2-tag
3. Visa innehållet i en p-tag
4. Styla komponenten med en ram och padding

<script setup>
// Implementera props här med validation

</script>

<template>
   <div class="preview-post">
      <h2><!-- Använd title prop här --></h2>
      <div class="post-body">
         <!-- Använd body prop här -->
      </div>
   </div>
</template>

<style scoped>
.preview-post {
/ Lägg till styling här /
}
</style>
