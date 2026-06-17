# Changelog

Alla noterbara ändringar i **Reptile Shop** dokumenteras här.
Formatet baseras på [Keep a Changelog](https://keepachangelog.com/) och versionerna
följer [Semantic Versioning](https://semver.org/lang/sv/) (MAJOR.MINOR.PATCH).

Detta är samma changelog som visas i spelets huvudmeny och som auto-updatern
hämtar från release-kanalen (`CasperW04/reptile-shop-releases`).

## [Unreleased]

### Planerat (nästa version — se `docs/3D-SHOP-PLAN.md`)
- Andra butiksexpansionen och fler inrednings-/möbeltyper.
- Riggade kund-NPC:er med gångloop (ersätter procedurell walk-bob).
- Leveranslådor med uppackning samt kontant-/växel-moment i kassan.
- Fler arter och resale av tillbehör utöver djur.

## [0.2.2] - 2026-06-17 — Alpha

### Fixed
- **Auto-update fungerar nu på riktigt.** I v0.2.0/v0.2.1 fanns updater-koden men
  var aldrig inkopplad — ingenting anropade den, så spelet kollade aldrig efter
  uppdateringar. Nu kollar spelet release-kanalen automatiskt i huvudmenyn vid
  start; finns en nyare version visas en banner ("Ny version tillgänglig: vX —
  Uppdatera nu") som laddar ner, sha256-verifierar och installerar (extern
  `Updater.bat` väntar in spelet, byter filerna och startar om).
- **OBS (engångsgrej):** din nuvarande build (≤ 0.2.1) saknar denna kontroll, så
  **v0.2.2 måste installeras manuellt en gång**. Därefter upptäcker spelet
  kommande versioner själv vid start.

## [0.2.1] - 2026-06-17 — Alpha

### Fixed
- **Förstaperson visas nu faktiskt.** v0.2.0 byggde förstapersons-världen men
  ritade fortfarande den gamla heltäckande UI-dashboarden ovanpå (opak,
  sortingOrder 100), så spelet såg ut precis som den gamla UI-versionen. Den
  gamla dashboarden byggs inte längre på spelvägen — du spawnar in i butiken i
  förstaperson med en transparent HUD (hårkors, prompt, plånbok/dag).
- Lade till ett PlayMode-regressionstest som bygger världen och säkerställer att
  ingen opak UI döljer 3D-vyn (skulle ha fångat v0.2.0-buggen).

## [0.2.0] - 2026-06-17 — Alpha

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

## [0.1.0] - 2026-06-17 — Alpha

Första spelbara alphan. Distribuerad som Windows-bygge till playtestare.

### Added
- Komplett kärnloop: **köp → föd upp → se morph → sälj → spara**.
- Mendelsk genetikmotor: recessiv, inkomplett-/ko-dominant + superformer,
  dominant, polygen och allel-komplex nedärvning, het-spårning (100/66/50 %)
  och automatisk combo-morph-namngivning.
- Tre arter: ball python, leopardgecko, kornsnok.
- Procedurellt renderade 3D-reptiler (runtime-mesh + ReptileSkin-shader) vars
  färg/mönster räknas ut deterministiskt från genotypen.
- Husbandry (hunger, hydrering, renlighet, temp/UVB) → hälsa & kvalitet,
  sjukdomshändelser och veterinärbehandling.
- Ekonomi: värderingsformel, direktförsäljning, marknadslistning och
  grossist-utförsäljning; dubbel valuta (Cash + Gems).
- Progression: shop-nivå 1–20 med upplåsningsgrindar (nivå + cash).
- Spara/ladda: versionerad JSON (genotyp sparas, fenotyp räknas om vid load).

[Unreleased]: https://github.com/CasperW04/reptile-shop/compare/v0.2.2...HEAD
[0.2.2]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.2
[0.2.1]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.1
[0.2.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.0
[0.1.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.1.0
