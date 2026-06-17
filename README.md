# Reptile Shop — Releases

Publik **distributions- och uppdateringskanal** för
[Reptile Shop](https://github.com/CasperW04/reptile-shop) (privat källkod, Sowandox AB).

Det här repot innehåller inte källkod — bara färdiga byggen och en versionsmanifest
som spelets inbyggda auto-updater läser.

## Hur uppdateringar fungerar

1. Varje nytt bygge publiceras som en **[Release](../../releases)** med Windows-zippen som bilaga.
2. `latest.json` (i repo-roten) pekar alltid på den senaste versionen:
   versionsnummer, nedladdnings-URL, storlek och `sha256`-checksumma.
3. Spelet hämtar `latest.json` vid start (utan inloggning — därför är repot publikt),
   jämför med sin egen version och erbjuder att ladda ner + installera uppdateringen.

Manifestets URL för klienten:
```
https://raw.githubusercontent.com/CasperW04/reptile-shop-releases/main/latest.json
```

## Installera manuellt

Ladda ner senaste `ReptileShop-Windows-*.zip` från [Releases](../../releases), packa upp
hela mappen och kör `ReptileShop.exe`. Om Windows SmartScreen varnar:
**"Mer information" → "Kör ändå"**.

## Changelog

Se [`CHANGELOG.md`](CHANGELOG.md).
