// === Dag 1: Övning 1 - Första Komponenten ===
/\*
ÖVNING: Min Första Vue-komponent
MÅL:

- Skapa din första Vue-komponent
- Förstå grundläggande komponentstruktur
- Använda template-syntax

INSTRUKTIONER:

1. Skapa en enkel välkomstkomponent
2. Använd template-syntax för att visa text
\*/
<template>
  <div class="welcome">
    <!-- Lägg till en välkomsthälsning här -->
  </div>
</template>

<script setup>
// Ingen avancerad logik än, bara grundläggande struktur
</script>

// === Dag 1: Övning 2 - Text Interpolation ===
/\*
ÖVNING: Personlig Profil
MÅL:

- Använda text interpolation
- Förstå hur man använder variabler i template
- Prova olika typer av interpolation

INSTRUKTIONER:

1. Skapa variabler för namn, ålder och intressen
2. Visa dessa i templaten med {{ }}
3. Prova att göra enkel matematik i interpolationen
\*/
<template>
  <div class="profile">
    <!-- Använd text interpolation här -->
    <h2><!-- Visa namn här --></h2>
    <p><!-- Visa ålder här --></p>
    <p><!-- Visa ålder om 5 år med enkel matematik --></p>
    <p><!-- Visa intressen här --></p>
  </div>
</template>

<script setup>
// Skapa dina variabler här
const name = 'Anna'
const age = 25
const hobbies = 'läsa, programmera, resa'
</script>

// === Dag 1: Övning 3 - Attribute Bindings ===
/\*
ÖVNING: Dynamiska Element
MÅL:

- Lära sig använda v-bind
- Förstå dynamiska attribut
- Prova olika typer av bindningar

INSTRUKTIONER:

1.  Skapa element med dynamiska attribut
2.  Använd v-bind för href, src och class
3.  Testa både fullständig syntax (v-bind:) och shorthand (:)
    \*/
    <template>
      <div class="dynamic-elements">
        <!-- Bind en länk -->
        <a v-bind:href="linkUrl"><!-- Länktext här --></a>

        <!-- Bind en bild -->
        <img :src="imageUrl" :alt="imageAlt">

        <!-- Bind en klass -->
        <div :class="containerClass">
          <!-- Innehåll här -->
        </div>

      </div>
    </template>

<script setup>
// Skapa variabler för dina bindningar här
const linkUrl = 'https://vuejs.org'
const imageUrl = '/path/to/image.jpg'
const imageAlt = 'En beskrivning'
const containerClass = 'container'
</script>
