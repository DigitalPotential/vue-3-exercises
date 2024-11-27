/\*
ÖVNING 5: Route Guards
MÅL:

- Förstå och implementera route guards
- Skydda vissa routes med auth-kontroll
- Hantera navigation baserat på auth-status

INSTRUKTIONER:

1. Skapa en enkel auth-service med login/logout
2. Implementera en global navigation guard
3. Skydda admin-sektionen med auth-check
4. Omdirigera unauthorized users till login

OBS: Detta är en avancerad övning som går utöver grundmaterialet
\*/

// router/index.js
router.beforeEach((to, from, next) => {
// Implementera auth-kontroll här
})

// auth.js
const auth = {
// Implementera basic auth-funktionalitet här
}
