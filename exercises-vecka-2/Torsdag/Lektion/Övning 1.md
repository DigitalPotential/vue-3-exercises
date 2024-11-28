Dessa övningar bygger på vue router uppgifterna 1-5
Om ni vill börjar från ett "facit repo" använd detta repo: https://github.com/DigitalPotential/vite-vue-router

/\*
ÖVNING 1: Route Transitions
MÅL:

- Lära sig använda transitions mellan routes
- Implementera olika transitions för olika routes
- Hantera transition-states

INSTRUKTIONER:

1. Implementera fade-transition mellan alla routes
2. Skapa en slide-transition för product-details
3. Lägg till loading-state animation
4. Gör transitions riktningsbaserade (slide left/right)

Tips: Använd <Transition> och CSS classes
\*/

// App.vue
<template>
<Transition name="fade" mode="out-in">
<RouterView />
</Transition>
</template>

<style>
    /* Implementera transitions här */
</style>
