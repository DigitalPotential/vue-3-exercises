/\*
ÖVNING 3: Advanced Meta Fields
MÅL:

- Använda meta fields för dynamisk sidtitel
- Implementera role-based access control
- Hantera route transitions baserat på meta
- Skapa breadcrumbs med meta data

INSTRUKTIONER:

1. Lägg till title och description i meta för alla routes
2. Skapa en Breadcrumb-komponent som använder meta data
3. Implementera role-based access (admin, user, guest)
4. Använd meta för att styra transitions

Tips: Kombinera meta fields med navigation guards
\*/

// Exempel på route config med meta
{
path: '/products',
meta: {
title: 'Products',
breadcrumb: 'Products',
requiresAuth: true,
roles: ['admin', 'user']
}
}
