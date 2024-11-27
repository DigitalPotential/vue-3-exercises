/\*
ÖVNING 4: Nästlade Routes
MÅL:

- Förstå och implementera nästlade routes
- Skapa en admin-sektion med sub-routes
- Hantera nästlad navigation

INSTRUKTIONER:

1. Skapa en Admin.vue komponent med en egen navigation
2. Skapa tre admin-undersidor: Dashboard, Users och Settings
3. Konfigurera nästlade routes för admin-sektionen
4. Implementera navigation mellan de nästlade routesen

OBS: Detta är en avancerad övning som går utöver grundmaterialet
\*/

// Admin.vue
<template>

  <div class="admin">
    <nav class="admin-nav">
      <!-- Admin navigation här -->
    </nav>
    <router-view></router-view>
  </div>
</template>
