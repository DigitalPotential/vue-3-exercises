/\*
ÖVNING 5: Error Handling
MÅL:

- Implementera error boundaries för routes
- Hantera 404 och andra error states
- Skapa recovery-mekanismer
- Visa loading och error states

INSTRUKTIONER:

1. Skapa en ErrorBoundary-komponent
2. Implementera async route loading med error handling
3. Visa loading states under route navigation
4. Lägg till retry-mekanismer för failed route loads

Tips: Använd onError hook och suspense
\*/

// Exempel på error boundary
<template>
<Suspense>
<template #default>
<RouterView />
</template>
<template #fallback>
<LoadingSpinner />
</template>
</Suspense>
</template>
