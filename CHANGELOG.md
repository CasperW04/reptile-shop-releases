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

## [0.3.55] - 2026-06-20 — Alpha — "Dekoration syns direkt 🌿"

### Fixed
- **🌿 Köpt dekoration syns nu direkt i terrariet** — växterna dyker upp i samma stund du köper en
  dekorationsnivå (tidigare först efter att vyn laddades om).

### Tested
- EditMode 627/627, PlayMode 63/63.

## [0.3.54] - 2026-06-20 — Alpha — "Storlekskrav per djur 📐"

### Added
- **📐 Varje djur visar sitt storlekskrav** i Djur-fliken: grön bock om terrariet räcker, röd varning
  om det är för litet — så du kan planera rätt boende.

### Tested
- EditMode 627/627, PlayMode 63/63.

## [0.3.53] - 2026-06-20 — Alpha — "Översikt i Djur-fliken"

### Added
- **📋 Summering i Djur-fliken:** rubriken visar nu antal djur i terrariet och hur många som är till salu.

### Tested
- PlayMode-test verifierar summeringsraden. EditMode 627/627, PlayMode 63/63.

## [0.3.52] - 2026-06-20 — Alpha — "Sköt alla 🧽"

### Added
- **🧽 "Sköt alla"-knapp** i terrariets Djur-flik: mata, vattna och städa alla djur i terrariet med
  ett klick — smidigt för terrarier/racks med flera djur.

### Tested
- PlayMode-test verifierar att alla djurs mätare återställs. EditMode 627/627, PlayMode 63/63.

## [0.3.51] - 2026-06-20 — Alpha — "Avlista alla"

### Added
- **🏷️ "Avlista alla"-knapp** i terrariets Djur-flik, bredvid "Lista alla till salu" — ta snabbt
  bort alla djur från försäljning igen.

### Tested
- PlayMode-test verifierar både listning och avlistning. EditMode 627/627, PlayMode 62/62.

## [0.3.50] - 2026-06-20 — Alpha — "Telefonens statusrad 📱"

### Added
- **📱 Telefonens hemskärm** visar nu en statusrad med aktuell dag och om butiken är öppen eller stängd.

### Tested
- PlayMode-test verifierar statusraden. EditMode 627/627, PlayMode 62/62.

## [0.3.49] - 2026-06-20 — Alpha — "Rykte i HUD:en ⭐"

### Added
- **⭐ Butikens rykte** visas nu i HUD:en bredvid antal djur till salu, så du ser hur nöjda kunderna är.

### Tested
- EditMode 627/627, PlayMode 62/62.

## [0.3.48] - 2026-06-20 — Alpha — "Väggskåp & matta 🧰"

### Added
- **🧰 Väggskåp och en kvadratisk matta** (nedladdade CC0, Kenney Furniture) inreder butiken ytterligare.

### Tested
- Planerar-test verifierar väggskåp + matta. EditMode 627/627, PlayMode 62/62.

## [0.3.47] - 2026-06-20 — Alpha — "Liv på minimapen 🔵"

### Added
- **🔵 Rörliga prickar på minimapen.** NPC:er (cyan) och bilar (orange) visas nu som prickar som rör
  sig i realtid på minimapen — staden lever även på kartan.

### Tested
- PlayMode-test verifierar att mover-prickar finns på minimapen. EditMode 626/626, PlayMode 62/62.

## [0.3.46] - 2026-06-20 — Alpha — "Till salu-räknare i HUD:en 🟢"

### Added
- **🟢 Antal djur till salu** visas nu i HUD:en (övre vänstra hörnet) och uppdateras direkt när du
  listar eller säljer ett djur.

### Tested
- EditMode 626/626, PlayMode 62/62.

## [0.3.45] - 2026-06-20 — Alpha — "Dekoration syns i terrariet 🌿"

### Added
- **🌿 Köpt dekoration syns nu i terrariet.** Varje dekorationsnivå lägger en liten växt inne i
  terrariet (upp till 3), så att köpen i Dekoration-fliken ger en synlig effekt — inte bara siffror.

### Tested
- PlayMode-test verifierar att rätt antal växt-props spawnas per dekorationsnivå. EditMode 626/626, PlayMode 62/62.

## [0.3.44] - 2026-06-20 — Alpha — "Riktning på minimapen 🧭"

### Added
- **🧭 Spelar-markören pekar åt blickriktningen** på minimapen, så du ser vart du är vänd.

### Tested
- PlayMode-test verifierar att markören följer blickriktningen. EditMode 626/626, PlayMode 61/61.

## [0.3.43] - 2026-06-20 — Alpha — "Minimap visar staden 🗺️"

### Added
- **🗺️ Stadens byggnader på minimapen.** Minimapen ritar nu ut stadens byggnader som grå prickar
  runt dig, så du ser kvarteren och hittar lättare i staden.

### Tested
- PlayMode-test verifierar att minimapen har byggnads-prickar. EditMode 626/626, PlayMode 61/61.

## [0.3.42] - 2026-06-20 — Alpha — "Vänthörna komplett ☕"

### Added
- **☕ Soffbord och pall** (nedladdade CC0, Kenney Furniture) kompletterar nu vänthörnan vid fåtöljen.

### Tested
- Planerar-test verifierar soffbord + pall. EditMode 626/626, PlayMode 61/61.

## [0.3.41] - 2026-06-20 — Alpha — "Fåtölj & växt 🪑"

### Added
- **🪑 Fåtölj och liten växt** (nedladdade CC0, Kenney Furniture) i butiken — en mysig vänthörna och
  mer grönska.

### Tested
- Planerar-test verifierar fåtölj + växt på golvet. EditMode 625/625, PlayMode 61/61.

## [0.3.40] - 2026-06-20 — Alpha — "Bokhylla i butiken 📚"

### Added
- **📚 Bokhylla** (nedladdad CC0, Kenney Furniture) står nu mot butikens bakvägg — mer inredd butik.

### Tested
- Nytt planerar-test verifierar bokhyllans placering mot bakväggen. EditMode 624/624, PlayMode 61/61.

## [0.3.39] - 2026-06-20 — Alpha — "Ljud när du listar 🔉"

### Added
- **🔉 Ljud-feedback** spelas nu när du lägger ut ett djur till försäljning (klick-ton), så prissättningen
  känns mer responsiv.

### Tested
- PlayMode-test verifierar att ljud-wiringen hanterar listnings-eventet utan fel. EditMode 623/623, PlayMode 61/61.

## [0.3.38] - 2026-06-20 — Alpha — "Lista alla till salu"

### Added
- **🏷️ "Lista alla till salu"-knapp.** I terrariets Djur-flik kan du nu med ett klick lägga ut alla
  djur i terrariet till försäljning samtidigt (varje djur behåller sitt påslag).

### Tested
- PlayMode-test verifierar att alla djur i terrariet listas. EditMode 623/623, PlayMode 60/60.

## [0.3.37] - 2026-06-20 — Alpha — "Panel-rubrik & stäng-knapp"

### Added
- **🏷️ Rubrik på terrarie-panelen** som visar terrariets namn + storleksklass högst upp.
- **✕ Stäng-knapp** på panelen så du kan stänga den med musen (utöver E/Esc).

### Tested
- PlayMode-test verifierar rubrik + stäng-knapp. EditMode 623/623, PlayMode 59/59.

## [0.3.36] - 2026-06-20 — Alpha — "Plånbok i dekor-fliken 💵"

### Added
- **💵 Pengar visas i Dekoration-fliken.** Terrariets Dekoration-flik visar nu hur mycket pengar du
  har, så du ser direkt om du har råd med nästa dekorationsnivå.

### Tested
- PlayMode-test verifierar att kontant-raden visas. EditMode 623/623, PlayMode 59/59.

## [0.3.35] - 2026-06-20 — Alpha — "Trafik 🚙"

### Added
- **🚙 Bilar som kör.** En del av stadens bilar rullar nu fram och tillbaka längs gatorna och vänder
  sig åt körriktningen — riktig trafik, inte bara parkerade bilar.

### Tested
- PlayMode-test verifierar att bilar kör i staden. EditMode 623/623, PlayMode 59/59.

## [0.3.34] - 2026-06-20 — Alpha — "Folk som går 🚶"

### Added
- **🚶 NPC:er som går runt.** Stadsgångarna strosar nu fram och tillbaka längs gatorna och vänder sig
  åt gångriktningen — staden lever, inte bara står still.

### Tested
- PlayMode-test verifierar att gångarna rör sig längs sitt gatusegment. EditMode 623/623, PlayMode 59/59.

## [0.3.33] - 2026-06-20 — Alpha — "Träd & lyktstolpar 🌳"

### Added
- **🌳 Stads-dekorationer.** Träd, buskar och lyktstolpar (nedladdade CC0 — Kenney Nature Kit +
  City Kit Roads) står nu utplacerade längs trottoarerna runt om i staden, så den känns mer levande.

### Tested
- PlayMode-test verifierar att stads-props placeras. EditMode 623/623, PlayMode 58/58.

## [0.3.32] - 2026-06-20 — Alpha — "För litet?-varning ⚠️"

### Added
- **⚠️ Varning för för litet terrarium.** I Djur-fliken visas nu en tydlig varning per djur om arten
  behöver ett större terrarium än det den står i ("⚠ För litet terrarium — behöver minst Stor"), plus
  terrariets storleksklass. Hjälper dig hålla djuren friska och värdefulla.

### Tested
- PlayMode-test verifierar att varningen visas för en stor art i ett litet terrarium. PlayMode 58/58,
  EditMode 623/623.

## [0.3.31] - 2026-06-20 — Alpha — "Dekorera terrariet 🪴"

### Added
- **🪴 Dekoration-fliken funkar.** Köp dekorationsnivåer (0→3) till ett terrarium mot pengar i
  **Dekoration**-fliken — varje nivå höjer terrariets **kvalitetstak** (värdefullare djur) och visar
  kvalitetsbonusen. Köp-knappen gråas ut om du inte har råd.

### Fixed
- **💾 Terrarium-storlek + dekoration sparas nu.** Storleksklassen (från det nya storlekssystemet) och
  dekorationsnivån persisteras korrekt över spara/ladda (storleken sparades inte tidigare).

### Tested
- PlayMode: köp höjer nivå + kvalitet och prisgate fungerar. EditMode: storlek + dekoration överlever
  spara/ladda. EditMode 623/623, PlayMode 57/57.

## [0.3.30] - 2026-06-20 — Alpha — "Sätt pris per djur 💰"

### Added
- **💰 Försäljningspris per enskilt djur.** I terrariets **Djur**-flik kan du nu för varje djur slå på
  **Till salu**, dra ett **påslags-reglage** och se det **begärda priset** live (marknadsvärde × påslag).
  Varje djur visar morf-namn, trivsel och marknadsvärde.

### Tested
- PlayMode-test verifierar pris-kontrollerna + att pris/listning sätts och eventet publiceras.
  EditMode 622/622, PlayMode 56/56.

## [0.3.29] - 2026-06-20 — Alpha — "Terrarium-panel med flikar"

### Added
- **🪟 Terrarium-meny med flikar.** Titta på ett terrarium och tryck **E** → en panel med tre flikar:
  **Djur** (listar djuren i terrariet + storleksklass), **Skötsel** (mata/vattna/städa/värme som förut)
  och **Dekoration** (kommande). Öppnas på Djur-fliken.
- **🖱️ Muspekaren frigörs** nu korrekt när terrarium-panelen öppnas (samma gate som dator/breeding).

### Tested
- PlayMode-test verifierar att panelen öppnas med tre flikar. EditMode 622/622, PlayMode 55/55.

### Kommer härnäst
- Sätt försäljningspris per enskilt djur i Djur-fliken, och dekorations-köp i Dekoration-fliken.

## [0.3.28] - 2026-06-20 — Alpha — "Minimap 🗺️"

### Added
- **🗺️ Minimap i hörnet.** En player-centrerad top-down-minimap (övre högra hörnet) visar din position
  (gul prick i mitten), butiken (grön markör) och väderstreck — så du hittar tillbaka i den stora staden.

### Tested
- PlayMode-test verifierar att minimapen byggs och spårar spelaren. EditMode 622/622, PlayMode 54/54.

## [0.3.27] - 2026-06-20 — Alpha — "Gator 🛣️"

### Added
- **🛣️ Riktiga gator.** Vägnät av nedladdade CC0-vägplattor (Kenney City Kit Roads, texturerade)
  läggs nu ut längs gatorna mellan kvarteren — bilarna står på riktiga vägar och staden har ett
  sammanhängande gatusystem.

### Tested
- PlayMode-test verifierar utlagda vägplattor. EditMode 622/622, PlayMode 53/53.

## [0.3.26] - 2026-06-20 — Alpha — "Riktiga gubbar 🧍"

### Added
- **🧍 Riktiga NPC-modeller!** Kunderna är nu riktiga nedladdade CC0-personer (Kenney Blocky Characters,
  fullt texturerade) istället för grå silhuetter — sex olika utseenden. Modellerna normaliseras
  automatiskt till människohöjd och ställs med fötterna på marken.
- **🚶 Folk i staden.** Gående NPC-gubbar står utplacerade på trottoarerna runt om i staden så världen
  känns befolkad.

### Tested
- PlayMode-test verifierar riktiga kundmodeller + stadsgångare. EditMode 622/622, PlayMode 53/53.

## [0.3.25] - 2026-06-20 — Alpha — "Bilar på gatorna 🚗"

### Added
- **🚗 Bilar i staden.** Riktiga nedladdade CC0-bilar (Kenney Car Kit) — sedan, SUV, taxi, skåpbil,
  polisbil m.fl., fullt texturerade — står nu parkerade längs gatorna mellan kvarteren.

### Tested
- PlayMode-test verifierar att bilar placeras i staden. EditMode 622/622, PlayMode 52/52.

## [0.3.24] - 2026-06-20 — Alpha — "EN STAD utanför butiken 🏙️"

### Added
- **🏙️ En hel stad runt butiken!** Kvarter av riktiga nedladdade CC0-byggnader (Kenney City Kit) —
  hus och skyskrapor — står nu runt och framför butiken, så världen känns levande när du tittar ut
  eller går ut genom dörren. Stor karta, massor av byggnader, deterministiskt utlagda.
- **🎨 Löst textur-pipelinen för nedladdade modeller.** Texturer bäddas nu in i .glb (via Blender) så
  byggnaderna renderas **fullt texturerade** (vita väggar, blå fönster) istället för platt/rosa.
  Detta låser upp framtida texturerade assets (bilar, fler byggnader, props).

### Tested
- PlayMode-test bygger staden och verifierar texturerade byggnader. EditMode 622/622, PlayMode 52/52.

### Kommer härnäst (samma kväll)
- Bilar, riktiga NPC-modeller (gubbar som går runt), gator, minimap — samt fortsättning på det nya
  terrarium-systemet (management-UI, pris per djur).

## [0.3.23] - 2026-06-20 — Alpha — "Nytt terrarium-system: storlekar spelar roll"

### Added
- **📐 Fyra terrarium-storlekar.** Nytt **XL Bioactive Vivarium** (4 platser) utöver Liten/Mellan/Stor —
  varje placerat terrarium har nu en storleksklass.
- **🐾 För litet terrarium straffar djuret.** Stora arter (hög vuxenvikt) som sätts i ett för litet
  terrarium blir trängda: deras temperatur-trivsel sjunker → sämre välmående → lägre hälsa → lägre värde
  och långsammare försäljning. Rätt storlek = friska, värdefulla djur.

### Tested
- Storleks-mappning (fixtur→storlek), penalty-kurvan och katalog-kontraktet (alla fyra storlekar finns +
  mappar rätt) testade. EditMode 622/622, PlayMode 51/51.

## [0.3.22] - 2026-06-20 — Alpha — "Nytt terrarium-system: storleks-grund"

### Added (under huven — första steget i det nya terrarium-systemet)
- **📏 Storleks-nivåer (grund).** `TerrariumSize` (Liten/Mellan/Stor/Extra stor) + regler som mappar en
  arts vuxenvikt till minsta nödvändiga terrarium-storlek, och om ett terrarium uppfyller kravet.
  (Kommande steg: storleks-fixturer + penalty om för litet, skötsel-UI, pris per djur.)

### Tested
- Nya tester för vikt→storlek-trösklar + Fits-regeln. EditMode 619/619, PlayMode 51/51.

## [0.3.21] - 2026-06-20 — Alpha — "Golvlampa"

### Added
- **🪔 Golvlampa.** En riktig CC0-golvlampa (Kenney) står nu mot höger vägg och sprider ett varmt
  ljus — mer mysig butiks-atmosfär, fungerande per-material-asset.

### Tested
- Nytt planerar-test verifierar golvlampans placering + varma ljus. EditMode 616/616, PlayMode 51/51.

## [0.3.20] - 2026-06-20 — Alpha — "Välkomstmatta"

### Added
- **🟫 Matta vid entrén.** En riktig CC0-matta (Kenney rugRounded, per-material-färgad så den texturerar
  korrekt) ligger nu platt på golvet precis innanför dörren — mer atmosfär, helt walkable.

### Tested
- Nytt planerar-test verifierar exakt en platt matta innanför entrén. EditMode 615/615, PlayMode 51/51.

## [0.3.19] - 2026-06-20 — Alpha — "Fler arter + texturpipeline"

### Added
- **🦎 ~30 fler verkliga reptilarter** (totalt 94): smaragdboa, anaconda, scharlakanskungssnok, fler
  geckos/ödlor/kameleonter/skinkar samt fler vatten- och landsköldpaddor (pannkaks-, egyptisk, burmesisk
  stjärn-sköldpadda m.fl.) — alla med samma artanpassade kropp/skötsel/avel.

### Under huven
- **Texturpipeline:** material-postprocessorn bevarar nu även base-color-**texturen** (+ UV-transform), inte
  bara färgen, när nedladdade .glb binds om till built-in Standard. Förberedelse för texturerade assets.

### Note (ärligt)
- **Stad utanför butiken pausad igen:** Kenney City Kit-byggnaderna använder en extern textur-atlas som inte
  band korrekt headless, och jag kan inte visuellt verifiera att de ser bra ut — så jag skeppar dem INTE
  förrän pipelinen är löst + du kan verifiera. (Möbel-/dekor-assets använder per-material-färger och funkar.)

### Tested
- EditMode 614/614, PlayMode 51/51.

## [0.3.18] - 2026-06-20 — Alpha — "Speltestar-fixar: terrarium, mus, butiksstatus"

### Fixed
- **✋ Går nu att sätta djur i TERRARIER (inte bara racks).** Terrariets glas-modell hade en mesh-collider
  med glipor som crosshair-strålen slank igenom — racks (utan modell-collider) fick en solid box och funkade.
  Nu får ALLA enclosures en solid box i full höjd, så strålen alltid träffar terrariet.
- **🖱️ Musen visas nu när du öppnar en breeding rack** (panelen frigör muspekaren + pausar input, som datorn).
- **🖥️ Datorns/skärmens hitbox** täcker nu hela datorn från golv till över skärmen.
- **🦵 Datorbordet har ben** (svävar inte längre).

### Added
- **🟢/🔴 Tydlig ÖPPEN/STÄNGD-status i HUD:en** (övre vänstra hörnet) så du alltid ser om butiken handlar.

### Note
- **Sälja/flytta utplacerade möbler finns redan:** gå in i bygg-läge (**B**), titta på möbeln och tryck
  **E** → välj Flytta/Förvara/Sälj. Terrarie-fixen ovan gör att det nu funkar på terrarier också.

### Tested
- EditMode 614/614, PlayMode 51/51.

## [0.3.17] - 2026-06-20 — Alpha — "Avel för alla arter"

### Added
- **🧬 Riktig avel för alla 65 arter.** Varje art har nu två klassiska recessiva morfer — **Albino**
  (amelanistisk, rubinögon) och **Anerythristic** (grå/silver) — så att para två het-djur ger 25%
  visuell morf enligt riktig mendelsk nedärvning. (Flaggskepps-arterna behåller sina egna kombo-morfer.)

### Tested
- Nytt test verifierar att varje katalog-art har båda generna; genetik-motorn hanterar dem.
  EditMode 614/614, PlayMode 51/51.

> Stad/exteriör: Kenney City Kit-byggnaderna använder en extern textur-atlas — pausat tills textur-
> pipelinen är löst så de inte blir otexturerade. Möbel-/dekor-assets (inbäddade texturer) fortsätter.

## [0.3.16] - 2026-06-20 — Alpha — "Riktiga ljud"

### Changed
- **🔊 Riktiga ljudeffekter (CC0).** Spelet använder nu nedladdade ljud från Kenney Interface Sounds
  (CC0) istället för syntade pip — för placering, försäljning (cha-ching), kläckning, skötsel, butik
  öppnar/stänger och UI-bekräftelser. Faller tillbaka på syntat ljud bara om ett klipp saknas.

### Tested
- Nytt test verifierar att alla CC0-ljudklipp finns i Resources. EditMode 613/613, PlayMode 51/51.

## [0.3.15] - 2026-06-20 — Alpha — "Telefon i hörnet"

### Added
- **📱 Smartphone i nedre högra hörnet — tryck `P`** för att öppna/stänga. Hemskärmen visar samma appar
  som datorn (Reptile Marketplace m.fl.), så du kan köpa/hantera på språng utan att gå till datorn.
  Tryck på en app → den öppnas i telefonen; "‹ Hem" går tillbaka; `Esc` stänger. Muspekaren frigörs och
  gameplay-input pausas medan telefonen är uppe (som datorpanelen).

### Tested
- Nytt PlayMode-test: telefonen installeras, exponerar de registrerade apparna och togglar öppen/stängd.
  EditMode 613/613, PlayMode 50/50.

> Obs: telefonens exakta UI-look finputsas i kommande iterationer (fal.ai-bakgrund/ikoner) — strukturen
> och flödet är verifierat, men det visuella bekräftas bäst i ditt Windows-bygge.

## [0.3.14] - 2026-06-20 — Alpha — "Varmare butik + riktiga assets"

### Changed
- **🎨 Varmare, inbjudande butiks-palett + ljusare/varmare ljus** (ljus ek-golv, varma väggar, off-white
  tak) istället för den grå "lådan".
- **🪴 Riktiga nedladdade 3D-assets:** golvdekoren använder nu en riktig CC0-krukväxt (Kenney Furniture
  Kit, CC0) istället för en egen-genererad modell — och fler växter (alla fyra hörn).

### Under huven
- Asset-pipeline etablerad: CC0-modeller laddas ner, verifieras headless via Blender-render (orientering/
  skala) och läggs i `Resources/Shop/`. Kenney-assets sparade i `Assets/Art/Kenney/` med CC0-licens.

### Tested
- EditMode 613/613, PlayMode 49/49.

## [0.3.13] - 2026-06-20 — Alpha — "65 verkliga arter + uppdaterings-fix"

### Fixed
- **🔁 Auto-uppdateringen fastnade ("går inte att uppdatera från 3.4").** Den interna versions-strängen
  frös på 0.3.4 (release-skriptet bumpade aldrig den), så varje bygge rapporterade 0.3.4 och uppdateraren
  erbjöd samma uppdatering i en evig loop. Nu bumpas versionen korrekt vid varje release — när du väl är
  på 0.3.13 är loopen bruten.

### Added
- **🦎 65 verkliga reptilarter** att stocka, placera, föda upp och sälja — ormar (majsorm, kungssnok,
  boa, pytonarter, grön trädpyton …), geckos (leopard, crested, gargoyle, tokay, leachianus …), ödlor
  (skäggagam, tegu, varaner, vattenagam …), kameleonter, skinkar, vatten-sköldpaddor och landsköldpaddor
  (sulcata, rysk, leopard, galápagos …). Varje art har artanpassad kropp, skötselprofil och pris.

### Tested
- Nya EditMode-tester verifierar att alla katalog-arter registreras och har giltig skötselprofil.
  EditMode 613/613, PlayMode 49/49.

## [0.3.12] - 2026-06-20 — Alpha — "Djurhantering 10/10: slutpass"

Sista av 10 iterationer som gör djurhantering + terrarie-placering genuint perfekt. Hela testsviten grön:
**EditMode 610/610, PlayMode 49/49** — där placerings-/hanteringsflödena drivs av tester som kör den
RIKTIGA runtime-kedjan (literala input-event → raycaster → tjänster), inte stubbar.

### Quality of life
- **🚫 Prompten säger tydligt "Fullt — ingen plats kvar"** när du siktar på ett fullt terrarium/rack med
  ett djur i handen, så du inte klickar i onödan.

### Hela loopen (0.3.3 → 0.3.12), kort
Placera från normalt avstånd · E öppnar skötsel överallt · djuret syns i terrariet · rack = avel /
terrarium = sälj · beläggning (2/4) i prompten · sålda djur försvinner · högerklick plockar upp ·
köp auto-väljer slot · konsekvent håll-tillstånd · full-terrarium-feedback.

## [0.3.11] - 2026-06-20 — Alpha — "Djurhantering 9/10: konsistent håll-tillstånd"

### Fixed
- **🔁 Att plocka upp ett djur tar nu bort modellen ur terrariet ordentligt** (ingen dubbel-rendering
  mot djuret-i-handen). Förut kunde upplockningen oavsiktligt återskapa world-modellen via ett slot-event.
- Härdat: ett djur med ogiltig slot (−1) försöker aldrig spawna en terrarie-modell.

### Quality of life
- **✋ Ett upplockat djur hålls direkt i handen** (hotbar-sloten väljs automatiskt), precis som vid köp —
  konsekvent håll-beteende genom hela loopen.

### Tested
- Nytt PlayMode-test verifierar att upplockning despawnar world-vyn OCH auto-väljer sloten.
  EditMode 610/610, PlayMode 48/48.

## [0.3.10] - 2026-06-20 — Alpha — "Djurhantering 8/10: hela loopen"

### Quality of life
- **🛍️ När du köper ett djur i Reptile Marketplace väljs hotbar-sloten automatiskt** — du håller direkt
  det du köpt och kan gå fram och placera det utan att leta efter rätt siffertangent.

### Tested
- Nytt end-to-end PlayMode-test driver HELA djurhanteringsloopen genom de riktiga tjänsterna:
  köp i marketplace → djuret hamnar i handen → placera i terrarium för försäljning → sälj (som en
  kund-checkout). Verifierar att pengar, lager och hotbar flödar rätt hela vägen. EditMode 610/610, PlayMode 47/47.

## [0.3.9] - 2026-06-20 — Alpha — "Djurhantering 7/10: plocka tillbaka djur"

### Added
- **🤚 Högerklicka på ett terrarium/rack för att plocka upp** det senast placerade djuret tillbaka i
  hotbaren — så du kan flytta om eller sälja det någon annanstans. Djuret avlistas från försäljning,
  slot:en frigörs och modellen tas bort ur terrariet (den syns i handen igen).

### Quality of life
- **⌨️ Kontroll-hinten visar nu placering & upplockning** ("Vänsterklick Placera · Högerklick Plocka upp"),
  på svenska, så hela hanteringsloopen är synlig längst ner.

### Tested
- Nytt PlayMode-test avfyrar det riktiga högerklick-inputet och verifierar att djuret återvänder till
  hotbaren (slot rensad, avlistad). EditMode 610/610, PlayMode 46/46.

## [0.3.8] - 2026-06-20 — Alpha — "Djurhantering 6/10: kunder köper & terrariet töms"

### Fixed
- **🛒 En såld reptil försvinner nu ur terrariet.** Förut despawnades aldrig modellen vid försäljning,
  så ett sålt djur låg kvar synligt för evigt. Nu töms platsen synligt när en kund köper djuret.
  (Bekräftat: ett djur du placerar "till försäljning" i ett terrarium är köpbart för kunder.)

### Quality of life
- **👁️ Synlig återkoppling i butiken** — terrariet visar korrekt vilka djur som faktiskt finns kvar
  att sälja, så lagret stämmer med verkligheten.

### Tested
- Nytt PlayMode-test verifierar att en reptils modell despawnas på `ReptileSoldEvent`.
  EditMode 610/610, PlayMode 45/45.

## [0.3.7] - 2026-06-20 — Alpha — "Djurhantering 5/10: platser & överblick"

### Quality of life
- **🔢 Placerings-prompten visar hur fullt det är** — "Vänsterklick: Placera till försäljning **(2/4)**" —
  så du ser direkt om det finns plats kvar i terrariet/racken innan du klickar.

### Tested
- Nytt PlayMode-test verifierar att placerings-målet exponerar sitt enclosure-index och att
  beläggningen ökar med ett per placering. EditMode 610/610, PlayMode 44/44.

## [0.3.6] - 2026-06-20 — Alpha — "Djurhantering 4/10: avel vs försäljning"

### Fixed
- **🧬 Att placera ett djur i en tub-rack seatar det nu för AVEL** (inte försäljning). Racks delade
  kategori med terrarier, så de routades fel till "till salu". Nu avgörs det av enclosure-typen.

### Quality of life
- **🪧 Placerings-prompten visar vad släppet gör** — "Vänsterklick: Placera **för avel**" vid en rack,
  "**till försäljning**" vid ett terrarium, så du vet innan du klickar.

### Tested
- Nytt PlayMode-test verifierar routningen via den riktiga katalogen (rack_2tub/rack_8tub → avel,
  terrarium_small/large → sälj). EditMode 610/610, PlayMode 43/43.

## [0.3.5] - 2026-06-20 — Alpha — "Djurhantering 3/10: reptilen syns i terrariet"

### Fixed
- **🦎 En reptil placerad från hotbaren syns nu FYSISKT inne i terrariet.** Förut landade djuret bara
  i databasen men ingen modell visades — koden återanvände "i-handen"-modellen, som förstörs när djuret
  lämnar hotbaren, så sloten blev tom. Nu spawnas en riktig world-modell i terrariets slot.

### Quality of life
- **💬 Placerings-toasten namnger djuret** — "Enigma placerad till försäljning." istället för en generisk text.

### Tested
- Nytt PlayMode-test placerar ett hotbar-djur och verifierar att en reptil-modell faktiskt parentas in
  i terrariets slot-ankare (childCount > 0). EditMode 610/610, PlayMode 42/42.

## [0.3.4] - 2026-06-20 — Alpha — "Djurhantering 2/10: skötsel överallt"

### Fixed
- **🩺 E på ett terrarium öppnar nu skötselpanelen även när crosshairet träffar fixtur-collidern.**
  Två interaktioner kunde sitta på samma objekt (bygg-läges-vyn + skötseln); raycastern tog förut bara
  den FÖRSTA (bygg-vyn, som inte gör något utanför bygg-läge) och skuggade skötseln. Nu väljer raycastern
  den **bästa** interaktionen (icke-tom prompt + högsta prioritet) på det man siktar på.

### Tested
- Nytt PlayMode-test bygger skugg-scenariot (bygg-vy + care på samma objekt) och kör den riktiga
  raycaster-scanningen — verifierar att skötseln fokuseras, inte bygg-vyn. EditMode 610/610, PlayMode 41/41.

## [0.3.3] - 2026-06-20 — Alpha — "Djurhantering 1/10: räckvidd + äkta verifiering"

Första av 10 iterationer som gör djurhantering + placering genuint perfekt. Fokus: verifiera den
RIKTIGA klick-kedjan (inget fejk-grönt) och göra placeringen mindre petig. EditMode 610/610, PlayMode 40/40.

### Changed
- **🖱️ Generösare placerings-räckvidd (3,5 m → 5 m).** Du kan nu släppa ett djur i terrariet från
  normalt stå-avstånd, inte bara på nära håll. Vänsterklick hanteras direkt från confirm-handlingen med
  egen räckvidd istället för att begränsas av interaktions-strålen.

### Tested (så det inte "låtsas funka")
- Nya integrationstester driver det **literala** `ConfirmPressed`-input-eventet genom hela kedjan
  (input → fan-out → raycast → placering) och verifierar att ett djur landar i terrariet både på
  1,5 m och **4,5 m** (bortom gamla räckvidden). Tidigare tester anropade en stub och missade detta.

## [0.3.2] - 2026-06-18 — Alpha — "Placering på riktigt"

Hotfix för speltestar-rapporten: det gick fortfarande inte att placera djur i terrariet.
EditMode 610/610, PlayMode 39/39 (nytt troget integrationstest som driver den RIKTIGA strålen
mot fixtur-collidern — det som tidigare tester missade).

### Fixed
- **✋ Gick fortfarande inte att lägga djur i terrarium/rack.** Ett placerat terrarium har TVÅ
  överlappande vyer: `EnclosureView` (där placerings-målet satt) och `PlaceableObjectView` (den
  solida footprint-collidern som crosshair-strålen oftast träffar). För det redan utplacerade
  start-terrariet kunde målet saknas på den vy strålen faktiskt träffade → tyst miss. Placeringen
  resolvar nu terrariet från **vilken som helst** av vyerna (läser enclosure-index direkt).
- **🖱️ Tydlig placerings-prompt** — när du håller ett djur och tittar på ett terrarium/rack visas
  nu "Vänsterklick: Placera djuret här", så det syns hur man gör (ingen meny behövs).
- **💬 Feedback istället för tyst miss** — klickar du med ett djur i handen utan att sikta rätt får
  du nu en hint ("Sikta på ett terrarium eller en rack och vänsterklicka") i stället för ingenting.

## [0.3.1] - 2026-06-18 — Alpha — "Allt funkar nu"

Buggfix-release med fokus på att allt faktiskt fungerar i körning, plus åtgärder från
speltestarnas rapport. EditMode 610/610, PlayMode 38/38 (riktiga flöden drivs i integrationstest).

### Fixed
- **✋ Gick inte att placera djur i terrarium / breeding rack** — interaktions- och placerings-
  komponenterna kopplades aldrig på de spawnade vyerna (AttachTo-seamsen anropades aldrig). Nu
  wirat via ett `WorldViewSpawnedEvent` så terrarier, breeding racks och disken blir interaktiva
  direkt de byggs.
- **🩺 E på ett terrarium** öppnar nu skötselpanelen (husbandry care).
- **🧬 E på disken** öppnar nu genetik-terminalen.
- **🕗 Klockan auto-öppnar nu butiken 08:00** (klock-modulen installerades före dygnscykeln och
  fick `null`-service → 08:00/18:00-hoppen blev tysta no-ops).
- **🖐️ Held-reptilen i handen** städas nu bort korrekt när handen töms (meshen blev kvar förut).
- **🧱 Bygg-ghosten** kunde felaktigt visa "OutOfBounds" på öppet golv (för snäv raycast-räckvidd).
- **🖱️ Musen syns nu i bygg-läget** så katalogen går att klicka (frigörs/återlåses vid på/av).
- **🪧 Butiksskylten** satt i dörröppningen — sitter nu på väggen bredvid entrén.
- **🟫 Kassadisken låg ner** — runtime laddade en gammal modell-kopia; nu står disken upp rätt.
- **🖥️ Datorns hitbox** täcker nu hela datorn inkl. skärmen, så crosshairet registrerar var du än siktar.

## [0.3.0] - 2026-06-18 — Alpha — "Dator, Marknad & Inventory"

Stort innehållslyft. EditMode 610/610, PlayMode 22/22.

### Added
- **🖥️ Dator i butiken** — vänsterklicka (eller E) på datorn för att öppna en dator-vy med appar.
- **🛒 Reptile Marketplace** — köp reptiler från andra uppfödare (genererade arter/morpher/het/
  kvalitet, säljare, pris). Köpta djur hamnar i ditt inventory.
- **🎒 9-slots hotbar-inventory** (Minecraft-stil) — växla med tangent **1-9** eller mushjul. Du
  **håller djuret i handen** (syns vid handen). Sparas i sparfilen.
- **✋ Placera från handen** — håll ett djur och titta på ett **terrarium → placeras för försäljning**;
  titta på en **breeding rack → placeras för avel**.
- **🕗 Klocka + veckodag** i HUD:en. Butiken **öppnar automatiskt 08:00**.
- **🌙 Dag-summering kl 18:00** (sålt / intäkter / kunder idag) med **Next Day → 07:45**.

### Changed
- Save-schema **v3** (additiva fält för inventory + klocka; gamla sparfiler migreras automatiskt).

## [0.2.12] - 2026-06-18 — Alpha

### Added
- **Öppna/stänga butiken med `O`** — det fanns ingen spelar-kontroll för att öppna butiken,
  så kunder kunde aldrig komma in. Nu öppnar/stänger du dagen med O.
- **Kontroll-hint på skärmen** — en alltid synlig rad längst ner visar tangenterna
  (WASD · E · B · O · Esc) så du alltid ser vad du kan göra.

### Fixed
- **Man fastnade på mattor/dekor** — dekor fick en blockerande collider. Nu går du över den
  (trigger-collider; fortfarande valbar i bygg-läget).
- **Kassan låg ner** — counter-modellen byggdes med höjden längs fel axel; nu står den upprätt.

## [0.2.11] - 2026-06-18 — Alpha

Stor kod-granskning: **44 buggar** hittade + adversariellt verifierade, ~40 fixade.
EditMode **422/422**, PlayMode 22/22, bygget grönt.

### Fixed (urval)
- **Läckor vid meny → nytt spel → meny (kritiskt):** moduler, objekt och event-prenumerationer
  städades inte → de staplades och kördes mot förstörda objekt (allt sämre ju fler omstarter).
  Nu rivs hela världen via en enda container, EventBus rensas och moduler Dispose:as korrekt.
- **Klockan synkade inte vid Load** — TimeService seedades aldrig från sparfilen + CurrentTick
  frös under spel → dag-räknaren drev isär.
- **Input aktiv i paus/meny** — B/E/vänsterklick/R påverkade världen bakom paus-overlayen.
- **Settings/Controls "Back"** gick alltid till huvudmenyn (även från in-game paus) → kunde
  råka starta nytt spel utan att spara.
- **Tutorial-deadlock** — steg 1 ("Walk to the counter") kunde aldrig slutföras.
- **Ekonomi:** daglig el-kostnad drogs aldrig; negativa köp/sälj gav gratis djur/pengar;
  kund-köp rullades aldrig som sannolikhet (varje chans = garanterad sälj).
- **Genetik:** recessiva allel-komplex-het:ar namngavs felaktigt som synliga morpher.
- **Placering:** slot-mappning använde fel formel (kunde radera giltiga placeringar vid load);
  roterade icke-kvadratiska terrarier hamnade snett.
- **Save:** autospara innan världen rivs vid byte; v1→v2-migration spawnade i hörnet.
- **Kunder/NavMesh:** kö-buggar, off-mesh-pathing, agent-warp-ordning, städning vid quit-to-menu.
- **Meny/uppdaterare:** video-RenderTexture frigjordes aldrig; upplösnings-dropdown defaultade fel;
  sha256-jämförelse + SemVer-kontrakt i auto-updatern.
- …och fler (~40 totalt).

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

[Unreleased]: https://github.com/CasperW04/reptile-shop/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.3.0
[0.2.12]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.12
[0.2.11]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.2.11
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
