## Reptile Shop — Alpha v0.2.0

Förstapersons-omtag: kärnsimuleringen (genetik, ekonomi, husbandry, avel,
sparning) är oförändrad men spelas nu genom en fysisk butik i förstaperson.

### Added
- **Förstaperson + fysisk butik:** gå runt i en startlokal (~8×6 m) och
  interagera med inredning, terrarier och stationer. En expansionsgrind
  låser upp mer yta vid shop-nivå 5.
- **Bygg- och placeringsläge:** rutnätsbaserad utplacering (0,5 m-celler) av
  hyllor, terrarier och inredning; köpt lagervara placeras direkt.
- **Kund-NPC:er:** kunder rör sig i butiken (NavMesh + procedurell walk-bob),
  väljer djur och kan påverka butikens rykte som i sin tur skalar trafiken.
- **Kassa:** enknapps-checkout (Confirm) för att slutföra en försäljning;
  återköp/refund ger 50 %.
- **Avelsstation:** para ihop två djur fysiskt i butiken och producera kull
  via den befintliga avelsmotorn.
- **Genetik-terminal:** läs av genotyp/het-spårning och morph-info i butiken.
- **Sparfiler/slots:** flera namngivna sparfiler – skapa, ladda, radera, kopiera.
- **Huvudmeny:** New Game / Continue / Load / Settings / Quit med changelog-panel.
- **Auto-update i appen:** spelet kollar release-kanalen vid start, jämför
  versioner och kan ladda ner + installera en nyare build.

### Unchanged
- Mendelsk genetikmotor, ekonomi/värdering, husbandry och spara/ladda-format
  är behållna oförändrade och nås nu via den fysiska butiken.
