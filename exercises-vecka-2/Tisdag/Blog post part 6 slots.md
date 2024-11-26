## Övning - Layout med Named Slots

### SCENARIOT:

Vi ska skapa en återanvändbar card-komponent som använder named slots
för att strukturera innehåll och actions i vår blog post creator.

### MÅL:

- Förstå hur named slots fungerar
- Skapa flexibla layout-komponenter
- Kombinera flera slot-typer

### INSTRUKTIONER:

1. Skapa en BaseCard komponent som:

   - Tar emot en title prop
   - Har en default slot för huvudinnehåll
   - Har en named slot för actions i header
   - Har grundläggande card-styling

2. Uppdatera App.vue för att:
   - Importera BaseCard
   - Wrappa PreviewPost och CreatePost i varsitt card
   - Lägga till relevant titel för varje card
   - Använda actions-slot för knappar/funktioner

### TIPS:

- Använd template #slot-name för named slots
- Tänk på att styling i card inte ska påverka innehållet
- Named slots ger flexibel layout-struktur
