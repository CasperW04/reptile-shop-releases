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
