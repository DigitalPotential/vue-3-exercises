/\*
ÖVNING 1: Grundläggande Routing
MÅL:

- Förstå grundläggande routing i Vue
- Skapa och konfigurera routes
- Använda router-link och router-view

INSTRUKTIONER:

1. Skapa tre komponenter: Home.vue, About.vue och Contact.vue med enkel text
2. Konfigurera routes för dessa komponenter
3. Skapa navigation med router-link
   \*/

// router/index.js
import { createRouter, createWebHistory } from 'vue-router'

const routes = [
// Implementera routes här
]

const router = createRouter({
history: createWebHistory(),
routes
})

export default router

// App.vue
<template>

  <div class="app">
    <nav>
      <!-- Implementera navigation här -->
    </nav>
    
    <!-- Lägg till router-view här -->
  </div>
</template>
