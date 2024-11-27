/\*
ÖVNING 2: Route Parameters
MÅL:

- Förstå och använda route parameters
- Hämta och visa parameter i komponenter
- Skapa dynamiska länkar

INSTRUKTIONER:

1. Skapa en ProductList.vue komponent som visar lista med produkter
2. Skapa en ProductDetails.vue komponent
3. Konfigurera en dynamisk route med parameter för product-id
4. Visa produkt-detaljer baserat på route parameter
   \*/

// ProductList.vue
<template>

  <div class="products">
    <!-- Lista produkter här med router-link till detaljer -->
  </div>
</template>

<script setup>
const products = [
  { id: 1, name: 'Laptop', price: 9999 },
  { id: 2, name: 'Phone', price: 5999 },
  { id: 3, name: 'Tablet', price: 4999 }
]
</script>

// ProductDetails.vue
<template>

  <div class="product-details">
    <!-- Visa produkt-detaljer baserat på route parameter -->
  </div>
</template>
