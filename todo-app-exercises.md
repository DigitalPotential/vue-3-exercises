# Todo App - Övningar

## Del 4 - Statistik

Lägg till en statistiksektion som visar information om todos.

1. Skapa computed properties för:
   - totalTodos (totalt antal)
   - completedTodos (antal klara)
   - remainingTodos (antal återstående)
   - completionRate (procent klara)
2. Skapa en stats-sektion i template med grid-layout
3. Visa alla statistikvärden med lämplig formatering
4. Styla stats-sektionen med bakgrundsfärg och avrundade hörn
5. Använd grid för att visa statistiken i fyra kolumner

Tips:

- Använd filter() för att räkna todos
- Använd Math.round() för procentberäkning
- Testa med olika antal todos för att verifiera beräkningarna

## Del 5 - Prioriterade todos

Lägg till möjlighet att markera todos som prioriterade.

1. Uppdatera todo-strukturen med en ny property `priority` (boolean)
2. Skapa en metod `togglePriority` som växlar prioritet för en todo
3. Lägg till en prioritet-knapp (⭐/☆) för varje todo
4. Styla prioriterade todos med en guldkant på vänster sida
5. Se till att nya todos skapas med `priority: false` som default

Tips:

- Använd conditional class binding för styling
- Emoji-stjärnorna ⭐ och ☆ kan användas för knappen

## Del 6 - Ta bort todos

Implementera funktionalitet för att kunna ta bort todos.

1. Skapa en metod `removeTodo` som tar bort en todo baserat på dess ID
2. Lägg till en ta bort-knapp (🗑️) för varje todo
3. Skapa en container för knappar (.todo-actions) som håller både prioritet- och ta bort-knappen
4. Styla ta bort-knappen med röd färg
5. Lägg till hover-effekt på ta bort-knappen

Tips:

- Använd filter() för att ta bort todo
- Gruppera knapparna med flex och margin-left: auto

## Del 7 - Mörkt läge

Lägg till ett mörkt tema som kan växlas.

1. Skapa en reaktiv variabel `isDarkMode` med ref()
2. Implementera en `toggleTheme` metod
3. Lägg till en tema-knapp i header (🌙/☀️)
4. Använd conditional styling för att ändra utseende i mörkt läge
5. Styla tema-knappen med rätt bakgrundsfärg beroende på läge

Tips:

- Använd v-bind för dynamiska klasser
- Testa olika färger för mörkt läge

## Del 8 - Reactive State Management

Refaktorera appen för att använda reactive() istället för flera ref().

1. Skapa ett reaktivt state-objekt med alla app-variabler
2. Uppdatera alla computed properties att använda state
3. Uppdatera alla metoder att använda state
4. Uppdatera template-bindningar till att referera state
5. Se till att all funktionalitet fortfarande fungerar som tidigare

Tips:

- Samla alla variabler i ett state-objekt
- Använd dot notation för att komma åt state properties
- Testa noga att allt fungerar som förväntat
