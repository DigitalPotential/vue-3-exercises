## Övning 5 - Komponenter med Slots

### SCENARIOT:

Vi ska skapa en återanvändbar knappkomponent med slots som kan användas
för olika formateringsalternativ i vår blog post creator.

### MÅL:

- Förstå hur slots fungerar
- Skapa återanvändbara komponenter
- Kombinera slots med props och events

### INSTRUKTIONER:

1. Skapa en BaseButton komponent som:

   - Tar emot en active prop (boolean)
   - Använder slot för knappens innehåll
   - Har grundläggande styling
   - Visar active state

2. Uppdatera CreatePost för att:
   - Importera BaseButton
   - Ersätta den befintliga bold-knappen med BaseButton
   - Skicka rätt props och events
   - Använda slot för "B" texten

### TIPS:

- Tänk på att slots ger flexibilitet för innehåll
- Kombinera slots med props för styling
- Behåll event-hantering i parent

### UTMANING:

- Lägg till en named slot för en ikon
- Skapa fler formateringsknappar med samma baskomponent
