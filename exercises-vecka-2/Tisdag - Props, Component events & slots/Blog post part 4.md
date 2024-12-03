## Övning 4 - Text Formatering med Props och Events

### SCENARIOT:

Vi ska lägga till en bold-funktion för titeln i vår blog post creator.
Användaren ska kunna växla mellan normal och bold text med en knapp,
och förändringen ska synas i både CreatePost och PreviewPost.

### MÅL:

- Fördjupa förståelsen för props och events
- Hantera delat state mellan komponenter
- Arbeta med CSS-klasser och conditional styling

### INSTRUKTIONER:

1. Uppdatera App.vue:

   - Lägg till state för att hålla koll på bold-status
   - Skicka bold-status som prop till båda komponenterna
   - Lyssna på uppdateringar av bold-status

2. Uppdatera CreatePost:

   - Lägg till en bold-knapp bredvid titel-input
   - Ta emot isBold som prop
   - Emitta ändringar i bold-status
   - Styla input baserat på bold-status

3. Uppdatera PreviewPost:
   - Ta emot isBold som prop
   - Applicera rätt styling baserat på bold-status
   - Sätt base font-weight till 200
   - Sätt bold font-weight till 800

### TIPS:

- Använd conditional class binding (:class)
- Tänk på att state ska hanteras i parent
- Använd CSS för visuella ändringar

### UTMANING:

- Lägg till fler formateringsalternativ (italic, underline)
- Gör knapparna toggleable (aktiv/inaktiv state)
