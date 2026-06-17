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

## [0.2.10] - 2026-06-18 — Alpha

### Added
- **Riktiga 3D-modeller i butiken** — Blender-konsten (terrarier, disk, hyllor, racks m.m.)
  renderas nu i spelet istället för greybox-klossar.
- **Breeder Racks i 4 storlekar** — Small (6 tubs), Medium (15), Large (30), Mega (50) i katalogen.
- **Tutorial** — 6-stegs guidning för nya spelare första gången.
- **Ny art: Western Hognose** (4:e arten) med egna gener och morpher.

### Fixed
- Art-import: `.glb`-material binds nu korrekt till built-in Standard-shadern (gltfast-importen
  triggade aldrig den gamla material-rebinden → allt låg på fel shader). Verifierat **0 URP-shaders**
  i bygget — ingen magenta.

## [0.2.9] - 2026-06-18 — Alpha

### Added
- **Riktig möbelkatalog** i bygg-läget (namngivna fixtures: terrarier, racks, disk,
  inkubator, avelsstation, terminal, hyllor, dekor) istället för greybox-fallback.
- **Kunder vill ha specifika morpher** — efterfrågan styrs av sällsynthet + värde.
- **Liv i butiken** — ormbunkar, hängande skyltar, pendellampor och varma ljus.
- **Ljud** — subtila cues vid placering, försäljning, kläckning, skötsel, dag öppna/stänga, UI.
- **Djupare avel/genetik** — rikare hatch-reveal + Punnett/het-utläsning i genetik-terminalen.
- **Ekonomibalans** — kundtrafik, hyra, priser och XP-pacing justerade.
- (Asset) **Breeder Rack-modell** (Small, 6 tubs) genererad i Blender — kopplas in i spelet i ett kommande steg.

### Changed
- Tester: EditMode 366/366, PlayMode 22/22 gröna.

## [0.2.8] - 2026-06-17 — Alpha

### Added
- **Settings fungerar nu:** fullscreen-läge, upplösningsval och VSync direkt i menyn.
- **Mark utanför butiken** — du faller inte längre ut i tomheten genom dörren.

### Fixed
- **Bygg-läget: klicka för att placera.** Vänsterklick placerar nu objektet (utöver
  E-tangenten, som var otillförlitlig), och **R** roterar ghosten innan du placerar.

## [0.2.7] - 2026-06-17 — Alpha

### Added
- **Discord:** en "Join our Discord"-knapp i menyns nedre hörn som öppnar vår
  officiella server.

### Changed
- Changeloggen visas nu som en liten scrollbar **UPDATES**-ruta uppe till höger i
  huvudmenyn (istället för en egen sida) och listar bara faktiska släppta versioner.

## [0.2.6] - 2026-06-17 — Alpha

### Added
- **Helt ny, proffsig huvudmeny:** loopande tecknad bakgrundsvideo (AI-genererad),
  spelets ikon som logga-badge, guld/emerald-tema, snyggare knappar med hover-effekt,
  och en **Controls-panel** med alla key bindings (WASD, mus, Shift, Ctrl, E, B, Esc).
- Spelets AI-genererade ikon används nu som app-/fönsterikon.

### Fixed
- **Bygg-läget gick inte att placera (allt rött).** Ett redundant, felplacerat
  greybox-golv (centrerat på origin) krockade med byggrutnätet (hörn-justerat mot
  ShopOrigin), så det mesta av det synliga golvet låg utanför bounds → röd ghost
  överallt. Nu byggs golvet bara av ShopShell (rutnäts-justerat) och spelaren
  spawnar inne i rummet — objekt går att placera.

## [0.2.5] - 2026-06-17 — Alpha

### Fixed
- **"Allt är magenta"-buggen fixad.** Miljön (golv, väggar, inredning) renderades
  helt rosa/magenta i Windows-bygget eftersom den inbyggda `Standard`-shadern
  strippades ur bygget — den refereras bara i runtime via `Shader.Find`, så Unity
  tog bort den och `Shader.Find` returnerade null. Bygget pinnar nu `Standard` +
  `Sprites/Default` så de alltid följer med. (Syntes aldrig i Mac-editorn, som har
  alla shaders inladdade — bara i den faktiska Windows-buildt.)

### Kontroller (påminnelse)
- **WASD** gå · **mus** titta · **E** interagera · **B** bygg-läge · **Esc** paus/meny.

## [0.2.4] - 2026-06-17 — Alpha

### Fixed
- **Changeloggen i huvudmenyn uppdateras nu.** Den bundlade kopian
  (`Resources/CHANGELOG.txt`) frystes vid v0.1.0 och synkades aldrig mot den riktiga
  changeloggen — nu kopierar bygget automatiskt root-`CHANGELOG.md` vid varje release,
  så menyns changelog alltid matchar den installerade versionen. (Den här texten ska
  alltså synas i menyns Changelog-panel om du kör 0.2.4.)

## [0.2.3] - 2026-06-17 — Alpha

### Added
- Versionsnumret visas nu i huvudmenyns nedre hörn, så du ser vilken build du kör.
- Testbygge som verifierar auto-update från v0.2.2: en v0.2.2-klient ska upptäcka
  denna version i menyn ("Ny version tillgänglig: v0.2.3") och kunna installera den
  själv — efter omstart visar hörnet `v0.2.3`.

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

[Unreleased]: https://github.com/CasperW04/reptile-shop/compare/v0.2.10...HEAD
[0.2.10]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.10
[0.2.9]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.9
[0.2.8]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.8
[0.2.7]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.7
[0.2.6]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.6
[0.2.5]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.5
[0.2.4]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.4
[0.2.3]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.3
[0.2.2]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.2
[0.2.1]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.1
[0.2.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.0
[0.1.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.1.0
