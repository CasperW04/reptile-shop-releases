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

## [0.84.0] - 2026-06-22 — Alpha — "Stamtavla + förändrings-staplar 🌳📊"

### Added
- **🌳 Pedigree / lineage-tracker** (Builder C/Husbandry) — ny app: välj ett djur och spåra dess släktträd
  (föräldrar + far-/morföräldrar) med en **inavels-varning** när föräldrarna var släkt. Sålda/avlivade anor
  visas som okända. Ren läs-modell över befintliga Sire/Dam-id (återanvänder InbreedingModel).
- **📊 Analytics: dagliga förändrings-staplar** (Builder D/Graphics) — Analytics-appen får ett stapeldiagram
  över daglig nettoförmögenhets-förändring (grön upp / röd ner), ritat från historiken via Painter2D.

### Tested
- EditMode 910/910, PlayMode 138/138 på merged main (PedigreeModel + bar-layout verifierade; konfliktfria merges).

## [0.83.0] - 2026-06-22 — Alpha — "Tillväxtkurvor + notis-filter 📈🔔"

### Added
- **📈 Growth Charts** (Builder C/Husbandry) — ny app: varje djurs vikt provtas **dagligen** och ritas som
  en kod-ritad sparkline med aktuell vikt + trend (▲/▼). "Weigh all now" tar en omedelbar avläsning. Hjälper
  upptäcka stadig tillväxt — eller ett oroande vikttapp — på ett ögonkast.
- **🔔 Notis-filter + olästa-badge** (Builder D/Graphics) — Notifications-flödet får **filter-chips**
  (All / 💰 Sales / 🥚 Hatches / 🏆 Achievements) och en **olästa-badge** ("N new") i headern som nollställs
  när appen öppnas.

### Tested
- EditMode 905/905, PlayMode 137/137 på merged main (WeightLogModel + notis-filter/olästa verifierade; konfliktfria merges).

## [0.82.0] - 2026-06-22 — Alpha — "Konsultation + tillgänglighet 🗣♿"

### Added
- **🗣 Customer Consultation & right-pet matching** (Builder C/Husbandry) — ny app: en kund anger
  **erfarenhetsnivå** (nybörjare/medel/expert) och **budget**. Rekommendera ett djur vars
  **skötselsvårighet** passar nivån och vars värde passar budgeten för en **konsultations-bonus** ovanpå
  försäljningen. Bättre matchning ger större bonus; ny kund varje dag.
- **♿ Tillgänglighet** (Builder D/Graphics) — ny **Display**-app med två sparade inställningar:
  **Reduced motion** (dämpar konfetti, kamera-shake, UI-fades) och **UI-skala** (75%→150%). Reduced motion
  respekteras av celebration-, kamerajuice- och notis-systemen.

### Tested
- EditMode 898/898, PlayMode 135/135 på merged main (7 nya ConsultationModel-tester + accessibility-gate; konfliktfria merges).

## [0.81.0] - 2026-06-22 — Alpha — "Pre-orders + kläck-kamera 📋🎥"

### Added
- **📋 Pre-Orders / Most-Wanted-tavla** (Builder C/Husbandry) — ny app: kunder lägger stående beställningar
  på en art med minst en viss kvalitet (★). Lämna över ett matchande eget djur för att **uppfylla** och få
  en **premie-belöning**. Tavlan fylls på dagligen och beställningar går ut om de inte fylls.
- **🎥 Kläck-kamerajuice** (Builder D/Graphics) — en ny kläckning ger nu en kort **kamera-shake + FOV-punch**
  (kod-driven game-feel), medvetet bara vid kläckningar (sällsynt, spännande), inte vid varje försäljning.

### Tested
- EditMode 887/887, PlayMode 133/133 på merged main (6 nya PreOrderModel-tester + kamera-modeller; flaky klock-test grönt på omkörning).

## [0.80.0] - 2026-06-22 — Alpha — "Brumation + kontroller ❄⌨️"

### Added
- **❄ Brumation** (Builder C/Husbandry) — ny app: kör en säsongsbunden nedkylnings-cykel (endast i kalla
  säsonger — höst/vinter) för att **förbereda djur för avel**, som den riktiga vinter-nedkylning många
  reptiler behöver. En genomförd cykel ger en temporär **fertilitets-bonus** (1.5×) i ett begränsat fönster.
- **⌨️ Controls-app** (Builder D/Graphics) — en in-game tangentbindnings-referens grupperad per kategori
  (Movement / Interaction / Building / Interface), speglar de verkliga bindningarna. (Live rebinding följer.)

### Tested
- EditMode 878/878, PlayMode 131/131 på merged main (konfliktfria merges; BrumationModel + kontroll-partition verifierade).

## [0.79.0] - 2026-06-22 — Alpha — "Kund-arketyper 🧑‍🤝‍🧑"

### Added
- **🧑‍🤝‍🧑 Kund-arketyper + guide** (Builder D/Graphics) — fem shopper-typer (Bargain Hunter 💸, Collector 🏆,
  Impulse ⚡, Browser 👀, Connoisseur 🧐), var och en med färg, ikon och tålamods-/budget-"tell", tilldelas
  deterministiskt per kund. Ny **Customer Guide**-app: en snabbnyckel till varje arketyp och vad de vill ha.
  (Diegetisk badge i världen är en uppföljning.)

### Tested
- EditMode 870/870, PlayMode 129/129 på merged main (deterministisk arketyp-tilldelning + komplett spridning; guide listar alla fem).

## [0.78.0] - 2026-06-22 — Alpha — "Enrichment + Analytics 🌿📊"

### Added
- **🌿 Enrichment & bioaktiv kvalitet** (Builder C/Husbandry) — ny app: investera per terrarium i
  **enrichment** (håller djuren i form, stabiliserar kroppskondition mot ideal dagligen) och en bioaktiv
  **städpatrull** (gråsuggor/hoppstjärtar som rensar smitta över tid). Välskötta terrarier blir lättare.
- **📊 Analytics-app** (Builder D/Graphics) — kod-ritad **nettoförmögenhets-trendlinje** + en
  **tillgångs-allokerings-paj** (kontanter/sparande/aktier) med legend, allt via Painter2D (inga bilder).
  Geometrin i en ren `ChartMath`.

### Tested
- EditMode 867/867, PlayMode 128/128 på merged main (konfliktfria merges; ChartMath + EnrichmentModel verifierade).

## [0.77.0] - 2026-06-22 — Alpha — "Kroppskondition + onboarding 💪🚀"

### Added
- **💪 Body Condition & feeding-response** (Builder C/Husbandry) — ny app: en veterinär-överblick per djur med
  kroppskondition (utmärglad → mager → ideal → överviktig → fet), matrespons (ivrig/villig/tveksam/vägrar)
  och en **Feed**-åtgärd. Mata hungriga bygger kondition; övermatning → fetma + vägran; vanvård → utmärgling.
  Deterministisk `BodyConditionModel`, per-djur, sparas.
- **🚀 Getting Started-checklista** (Builder D/Graphics) — ny app: en guidad första-sessions-checklista
  (placera terrarium, lägg till reptil, dekorera, första försäljning, spara ihop $5 000) som bockar av sig
  själv live, visar progress och kan döljas (sparas).

### Tested
- EditMode 857/857, PlayMode 126/126 på merged main (konfliktfria merges; flaky klock-test grönt på omkörning).

## [0.76.0] - 2026-06-22 — Alpha — "UI-juice ✨"

### Added
- **✨ UI-juice** (Builder D/Graphics) — återanvändbara `UiJuice`-helpers för dator-apparna: animerade
  **count-up**-siffror (ease-out), **pop**-overshoot, **fade-in** och pop-scale. Notifications-flödet
  fadar nu in sina rader. Mer liv i gränssnittet, helt kod-drivet.

### Tested
- EditMode 847/847, PlayMode 124/124 på merged main (count-up/pop/fade verifierade; konfliktfri merge).

## [0.75.0] - 2026-06-22 — Alpha — "DNA-labb 🧬"

### Added
- **🧬 DNA Lab** (Builder C/Husbandry) — ny app: istället för att prov-para kan du betala en avgift för att
  direkt **bevisa ut** ett djurs dolda (möjliga) het-anlag. Varje obevisat het löses till antingen
  **bekräftad bärare** eller **rensat** — deterministiskt, viktat mot dess het-sannolikhet (66% het bevisas
  ut ~66% av gångerna). Skriver tillbaka i genotypen; testade djur spåras + sparas.

### Tested
- EditMode 847/847, PlayMode 120/120 på merged main (7 nya DnaTestModel-tester + app-nåbarhet; konfliktfri merge).

## [0.74.0] - 2026-06-22 — Alpha — "Golden hour 🌅"

### Added
- **🌅 Ljus-stämningar + animerad dimma** (Builder D/Graphics) — omgivningsljuset värms nu till en
  **golden-hour-amber** kring gryning (~06) och skymning (~18), ovanpå dygn/säsong/väder (neutralt mitt på
  dagen/natten). **Animerad dimma**: diset andas in/ut över tid (±12% sikt) istället för statiskt. Allt
  kod-drivet, inga assets. (Värmelamps-glöd är en uppföljning.)

### Tested
- EditMode 840/840, PlayMode 119/119 på merged main (golden-hour byggde rent ovanpå integratorns säsong/väder-kod, auto-merge).

## [0.73.0] - 2026-06-22 — Alpha — "Biosäkerhet 🧫"

### Added
- **🧫 Biosäkerhet & smitta** (Builder C/Husbandry) — en smittsam åkomma (kvalster/sjukdom) sprids nu dagligen
  mellan samboende djur; **karantän**-satta djur varken smittas eller smittar, och utbrott startar organiskt.
  Ny **Biosecurity**-app: se infekterade vs karantän-satta + "Treat all" för att bota mot en avgift per djur.
  Deterministisk `ContagionModel` tickad dagligen; smitt-/karantänstatus sparas.

### Tested
- EditMode 837/837, PlayMode 118/118 på merged main (6 nya ContagionModel-tester + app-nåbarhet; konflikt löstes på Builder C:s domän-partial, övrigt rent).

## [0.72.0] - 2026-06-22 — Alpha — "Parallellt skördat: inkubation + notiser 🥚📨"

_Första parallella integrationen: 2 builders (Husbandry + Graphics) levererade samtidigt, mergade konfliktfritt via partial-sömmarna._

### Added
- **🥚 Incubation Planner** (Builder C/Husbandry) — ny app: välj inkubationstemperatur och se förutsagd
  kläck-**könsfördelning** (svalare = fler honor, varmare = fler hanar) + **äggdödlighets-risk** (lägst i
  idealbandet, stiger mot extremerna). Hjälper avelsplanering. Deterministisk `IncubationModel`.
- **📨 Notifications Center** (Builder D/Graphics) — ny app: ett beständigt, nyast-först-flöde över vad som
  hänt (försäljningar 💰, kläckningar 🥚, achievements 🏆), capat till senaste 50, sparas mellan sessioner.
- **🎉 Celebration juice** (Builder D/Graphics) — achievement-upplåsning ger nu en kod-driven konfetti-burst
  (primitiver, seedade hastigheter, gravitation, auto-despawn) + `CountUpModel` för animerade siffror.

### Tested
- EditMode 831/831, PlayMode 117/117 på merged main (alla builders' nya tester gröna; noll merge-konflikter).

## [0.71.0] - 2026-06-22 — Alpha — "Co-op chat 💬"

### Added
- **💬 Co-op chat** — spelarna kan skicka korta textmeddelanden till varandra över co-op-anslutningen
  (`SendChat`/`OnChatReceived` på både host och klient, via samma transport-söm). Grunden för att
  kommunicera i delad butik.

### Changed (infra)
- **Integrator-säkerhetsnät**: ett PlayMode-test öppnar nu VARJE registrerad dator-app och säkrar att den
  bygger sitt fönster utan krasch — fångar en trasig app från någon parallell builder före release.

### Tested
- EditMode 822/822 (chat åt båda håll, tom chat ignoreras), PlayMode 112/112 (alla ~28 appar bygger fönster).

## [0.70.1] - 2026-06-22 — Alpha — "Save-bakåtkompat 💾"

### Added (infra)
- **💾 Bakåtkompatibilitets-guard** — ett test som säkrar att saves skapade innan en feature fanns (nya
  samlingar saknas i filen) ändå laddar utan krasch, med säkra tomma defaults. Sätter kontraktet alla
  parallella builders följer när de lägger ett persisterat fält.

### Tested
- EditMode 820/820 (gammal save med null-samlingar → laddar, defaultar StockHoldings/Quotes/Orders/Shorts/Options/Bonds/NetWorthHistory till tomma).

## [0.70.0] - 2026-06-22 — Alpha — "Parallell-redo 🧵"

### Changed (infra)
- **🧵 Parallell-utvecklingsrigg** — wiring-filerna (`GameState`, `SaveGame`, `SaveMapper`,
  `ComputerAppsModule`, `ModuleWiring`) är nu `partial` med per-domän-sömmar (Economy/Husbandry/Graphics),
  så flera utvecklare kan jobba samtidigt utan att krocka i delade filer. Worktree-script
  (`tools/parallel/new-worktree.sh`), workflow + tilldelningar (`docs/PARALLEL-WORKFLOW.md`,
  `docs/PARALLEL-ASSIGNMENTS.md`) och CHANGELOG-fragment (`docs/changes/unreleased/`) tillagda. Möjliggör
  1 integrator + 3 builders i isolerade worktrees mot en enda versionslinje.

### Tested
- EditMode 819/819, PlayMode 111/111 — sömmarna är no-ops tills domän-filer fyller dem; alla appar/moduler registreras oförändrat.

## [0.69.0] - 2026-06-22 — Alpha — "Årstider 🍂"

### Added
- **🍂 Årstider** — spelet har nu en årscykel (Vår/Sommar/Höst/Vinter, 15 dagar var) som tonar butikens
  omgivnings-palett: frisk vår, varm sommar, bärnstensfärgad höst, sval vinter — ovanpå dygnscykeln och
  vädret. Tillsammans ger de tre systemen en levande värld, helt kod-drivet utan nya assets. (Research-backlog.)

### Tested
- EditMode 819/819 (säsong cyklar genom fyra + wrappar till nytt år, dag-i-säsong), PlayMode 111/111 (vinter-ambient svalare/blåare än sommar).

## [0.68.0] - 2026-06-22 — Alpha — "VIP-stamkunder 🤝"

### Added
- **🤝 Lojala VIP-stamkunder** — ett växande underlag av återkommande kunder (skalar med butikens rykte,
  upp till 30) som ger en liten stadig passiv intäkt varje dag via upprepade order. Belönar att bygga rykte
  och balanseras av företagsskatten. VIP-antal visas i Dashboard. (Research-backlog.)

### Tested
- EditMode 816/816 (VIP-antal skalar+capar med rykte, daglig intäkt 0 utan VIP/positiv med + deterministisk, krediterar kassan), PlayMode 110/110.

## [0.67.0] - 2026-06-22 — Alpha — "Levande djur 🫁"

### Added
- **🫁 Reptil-andning** — djuren andas nu med en subtil, kod-driven skal-puls (±1,5%), med en egen fas per
  djur så ett helt terrarium inte andas i takt. Små men stora skillnaden mellan "staty" och "levande".
  (Research-backlog: game-feel/grafik. Blink + tungspetsning är en uppföljning.)

### Tested
- EditMode 813/813 (andnings-skala håller sig inom amplitud, olika faser desynkar, oscillerar över tid), PlayMode 110/110.

## [0.66.0] - 2026-06-22 — Alpha — "Sälj-juice 💰"

### Added
- **💰 Sälj- & kläck-feedback** — varje försäljning och varje kläckning ger nu en festlig, belopps-skalad
  toast ("Sold for $X" → "💰 Sold for $X!" → "💰💰 BIG SALE — $X! 🎉") plus kassa-chime. De två stora
  positiva ögonblicken känns nu. (Research-backlog: game-feel.)

### Tested
- EditMode 810/810 (tier skalar med pris, toast-text per tier, kläck-toast), PlayMode 110/110 (sälj-/kläck-event ger rätt toast via polish-modulen).

## [0.65.0] - 2026-06-22 — Alpha — "Företagsskatt 🧾"

### Added
- **🧾 Företagsskatt** — en återkommande wealth-sink som balanserar alla nya inkomstkällor: var 10:e dag
  beskattas 5% av kassan över ett fribelopp på $10 000. Bank-appen visar nästa skattedag + uppskattat
  belopp. (Research-inspirerad: sinks vs faucets.)

### Tested
- EditMode 807/807 (skatt bara var 10:e dag, fribelopp exkluderas, dras på rätt dag, nästa-skattedag), PlayMode 109/109.

## [0.64.0] - 2026-06-22 — Alpha — "Alerts 🔔"

### Added
- **🔔 Alerts-app (smart varningscenter)** — en deduperad, allvarlighets-ordnad lista över vad som behöver
  din uppmärksamhet: sjuka djur (kritiskt), djur som behöver vård, låg kassa, lån som löper med ränta,
  ömsande djur. Ersätter notis-spam med en åtgärdbar feed. (Research-backlog.)

### Tested
- EditMode 803/803 (frisk rik butik = inga larm, sjuka djur = kritiskt + antal, låg kassa/lån = varningar, ordning, null-säker), PlayMode 109/109.

## [0.63.0] - 2026-06-22 — Alpha — "Portfölj-försäkring 🛡"

### Added
- **🛡 Portfölj-försäkring** — en hedge mot börskrascher: betala en liten daglig premie (0,6% av portföljen)
  och få en kompensation (7% av portföljen) varje krasch-dag. Slå på/av i Stocks-appen. Knyter ihop
  försäkring med de befintliga marknads-events. (Research-backlog.)

### Tested
- EditMode 799/799 (oförsäkrad = ingen effekt, normal dag = bara premie, krasch-dag = nettoutbetalning), PlayMode 108/108.

## [0.62.0] - 2026-06-22 — Alpha — "Mål 🎯"

### Added
- **🎯 Goals-app: långsiktiga milstolpar** — 10 stora mål som binder ihop alla system (nå $100k/$1M
  nettoförmögenhet, äg 20 djur, föd upp 50, sälj 100, $5k-försäljning, 10 achievements, $50k aktieportfölj,
  butiksnivå 5, dag 50) med kod-ritade progress-barer som uppdateras live. Ger riktning bortom dagsmålet.
  (Research-backlog.)

### Tested
- EditMode 796/796 (mål unika, progress/done följer state + klampar, completed-count), PlayMode 108/108 (appen speglar uppnådda milstolpar).

## [0.61.0] - 2026-06-22 — Alpha — "Bulk-åtgärder 📦"

### Added
- **📦 Bulk-åtgärder i Animals-rostern** — agera på hela det filtrerade urvalet på en gång istället för ett
  djur i taget: "List shown" / "Unlist shown" (sätt/ta bort till-salu) och "Markup 1.2× / 1.5×". Kombinera
  med filter (t.ex. visa hanar → lista alla) för snabb butikshantering. (Research-backlog.)

### Tested
- EditMode 793/793 (set-for-sale ändrar bara de som behövs, markup klampas + appliceras, null-säker), PlayMode 107/107 (bulk listar exakt de visade hanarna).

## [0.60.0] - 2026-06-22 — Alpha — "Pairing Planner 🧬"

### Added
- **🧬 Pairing Planner + inavels-koll** — välj två av dina djur och se deras släktskap (från stamtavlan:
  föräldrar, hel-/halvsyskon, far/morföräldrar) med en tydlig varning (säker / viss risk / stark
  inavelsrisk) innan du parar dem. Ny app. (Research-backlog.)

### Tested
- EditMode 790/790 (förälder-barn 0.5, helsyskon 0.5, halvsyskon 0.25, far/morförälder 0.25, obesläktad 0, varnings-nivåer), PlayMode 106/106 (appen flaggar syskon-par).

## [0.59.0] - 2026-06-22 — Alpha — "Optioner 🎟️"

### Added
- **🎟️ Optioner (calls & puts)** — hävstångs-satsningar på börsen: köp en 7-dagars at-the-money call (tjänar
  om kursen stiger över strike) eller put (tjänar om den faller). Du betalar en premie nu (vol-/tids-baserad);
  vid förfall betalas eventuell vinst ut automatiskt, annars förfaller den värdelös. Köp i Stocks-appen.
  Ännu ett lager på det överdrivet välutvecklade börssystemet. (Research-backlog.)

### Tested
- EditMode 785/785 (premie positiv + skalar med vol/tid, call betalar över strike, put under, OTM förfaller noll, ej innan term, persistens), PlayMode 105/105.

## [0.58.0] - 2026-06-22 — Alpha — "Index-fond 🧺"

### Added
- **🧺 Reptil-index-fond (RIDX)** — en diversifierad investering vars kurs är snittet av hela marknaden.
  Lägre volatilitet än en enskild aktie (bevisat i test) — den säkrare delen av risk-spektrumet bredvid
  enskilda aktier, blankning och obligationer. Köp/sälj högst upp i Stocks-appen. (Research-backlog.)

### Tested
- EditMode 781/781 (index = marknadssnitt + inom min/max, köp/sälj via index-pris, svänger mindre än en volatil aktie över 60 dagar), PlayMode 105/105.

## [0.57.0] - 2026-06-22 — Alpha — "Dashboard 📊"

### Added
- **📊 Dashboard-app** — ett finansiellt kommandocenter: stat-rutor (kassa, nettoförmögenhet, peak,
  portfölj, livstidsförsäljning/intäkt, uppfödda djur, bästa försäljning) + en **kod-ritad
  förmögenhetsgraf** (staplar från daglig historik, helt via VisualElement — ingen charting-lib, inga
  assets). (Research-backlog #2.)

### Tested
- EditMode 778/778, PlayMode 105/105 (stat-rutor visas, en graf-stapel per historik-punkt).

## [0.56.0] - 2026-06-22 — Alpha — "Djur-roster 🦎"

### Added
- **🦎 Animals-app: sökbar/sorterbar/filtrerbar djur-roster** — hitta rätt djur på sekunder i en växande
  samling: sök på namn/art, filtrera (Till salu / Behöver vård / Sjuk / Ömsar / Hanar / Honor / Bevisade)
  och sortera (Namn / Art / Äldst / Vikt / Kvalitet / Hälsa). Visar hälsa, välmående, vikt, stjärnor.
  (Första featuren ur den nya research-backloggen — `docs/RESEARCH-BACKLOG.md`.)

### Tested
- EditMode 778/778 (filter/sök/sortering korrekt över fixtur-roster), PlayMode 104/104 (app nåbar, speglar samlingen + sök).

## [0.55.0] - 2026-06-22 — Alpha — "Obligationer 🏦"

### Added
- **🏦 Obligationer / bundet sparande** — lås en summa i banken på fast tid för garanterad högre avkastning:
  7 dagar +8%, 14 dagar +20%, 30 dagar +50%. Kan inte tas ut i förtid (avvägningen mot det fria
  sparkontot). Mognar automatiskt och betalas ut vid förfallodagen.

### Changed
- **Bank-appen är nu på engelska** (speltestar-feedback om engelskt UI).

### Tested
- EditMode 773/773 (längre löptid ger mer, köp drar kapital, mognar vid förfall ej innan, persistens), PlayMode 103/103.

## [0.54.0] - 2026-06-22 — Alpha — "Förmögenhets-trend 📈"

### Added
- **📈 Nettoförmögenhets-historik + peak** — spelet sparar din nettoförmögenhet per dag (capad historik) och
  din all-time topp. Stocks-appen visar nu en liten trend-sparkline + din peak, så du ser om imperiet växer
  eller krymper över tid.

### Tested
- EditMode 768/768 (historik capas, peak spåras + sjunker aldrig, persistens), PlayMode 103/103.

## [0.53.0] - 2026-06-22 — Alpha — "Daglig quiz ❓"

### Added
- **❓ Daglig reptil-quiz** — en ny app med en roterande trivia-fråga per speldag (12 frågor om reptiler &
  skötsel). Svara rätt och tjäna $150 — ett svar per dag. Lite kul lärande + en liten daglig inkomst.

### Tested
- EditMode 766/766 (frågebank giltig, deterministisk per dag, belönar rätt en gång/dag, persistens), PlayMode 103/103 (app nåbar, rätt svar betalar en gång).

## [0.52.0] - 2026-06-22 — Alpha — "Nettoförmögenhet 💼"

### Added
- **💼 Nettoförmögenhet** — ett samlat tal som binder ihop alla pengasystem: kontanter + sparande +
  aktieportfölj + orealiserad short-P/L − utestående lån. Visas i Stocks-appen så du ser hela din
  finansiella bottom line på ett ställe.

### Tested
- EditMode 761/761 (summerar cash/sparande/portfölj − lån, inkluderar short-P/L, null-säker), PlayMode 102/102.

## [0.51.0] - 2026-06-22 — Alpha — "Väder ⛅"

### Added
- **⛅ Dynamiskt väder** — varje speldag har ett deterministiskt väder (Sunny/Cloudy/Rain/Storm) som tonar
  scenens dimma: klar, lång sikt en solig dag; tät, dyster närhet i storm. Ger dagarna olika känsla
  tillsammans med dygnscykeln. Kod-drivet, inga nya assets.

### Tested
- EditMode 758/758 (väder deterministiskt, alla typer förekommer, dimma tätnar med oväder), PlayMode 102/102 (storm-dimma närmare än sol).

## [0.50.0] - 2026-06-22 — Alpha — "Blankning 📉"

### Added
- **📉 Blankning (short selling)** — satsa MOT en aktie: "Short" lånar och säljer aktier till nuvarande
  kurs; faller kursen tjänar du mellanskillnaden när du "Cover":ar, stiger den förlorar du. Kräver
  marginal (kontanter ≥ positionens värde) som säkerhet. Öppnar/coverar i Stocks-appen med live P/L.
  Ännu ett lager på det överdrivet utvecklade börssystemet.

### Tested
- EditMode 754/754 (short tjänar när priset faller, förlorar när det stiger, margin-krav, persistens), PlayMode 101/101.

## [0.49.0] - 2026-06-22 — Alpha — "Daglig bonus 🎁"

### Added
- **🎁 Daglig login-bonus** — varje ny speldag får du ett litet kontant-stipendium som växer med en
  streak av dagar i rad ($200 → upp till $440 vid 7 dagar i rad), och nollställs om du hoppar över en dag.
  Delas ut automatiskt vid dygnsskiftet. En mjuk inkomst-floor + anledning att komma tillbaka.

### Tested
- EditMode 750/750 (bonus-trappa + cap, en gång per dag, streak ökar/nollställs, persistens), PlayMode 101/101.

## [0.48.0] - 2026-06-22 — Alpha — "Fler achievements 🏆"

### Added
- **🏆 7 nya achievements** — Millionaire ($1M), Dynasty (föd upp 100 djur totalt), Big Score (enskild
  försäljning $5 000+), Sales Veteran (sälj 100 totalt), Investor (äg aktier), Stock Mogul (aktieportfölj
  $50 000), Month One (nå dag 30). Knyter ihop avel, försäljning och börsen.

### Changed
- **Alla achievement-namn + beskrivningar är nu på engelska** (speltestar-feedback om engelskt UI).

### Tested
- EditMode 746/746 (katalog engelsk + unika id:n), PlayMode 101/101 (nya tröskel-achievements awardas från servicen).

## [0.47.0] - 2026-06-22 — Alpha — "Cricket Casino 🎰"

### Added
- **🎰 Cricket Casino** — en ny enarmad bandit-app att spela med butikskassan. Välj insats ($50/$200/$1000),
  spinn tre hjul: tre lika ger stor utbetalning (💎×20 högst), två lika ger insatsen tillbaka, annars förlust.
  Riktig house edge (på sikt förlorar man) så det är ett kul money-sink, inte en pengamaskin.

### Tested
- EditMode 744/744 (paytable + bevisad house edge över 5000 spins), PlayMode 100/100 (insats debiteras via ekonomin; spelaren är back över en lång session).

## [0.46.0] - 2026-06-22 — Alpha — "Dag & natt 🌗"

### Added
- **🌗 Dag/natt-stämning** — butikens omgivningsljus följer nu spelklockan: varmt och ljust vid lunch,
  gradvis nedtonat till ett svalt, månljust dunkel på natten. Helt kod-drivet (skalar bas-ambient + en
  kall nattnyans) — inga nya 3D-assets. Ger dygnet en känsla utan att tappa läsbarhet (aldrig kolsvart).

### Tested
- EditMode 741/741 (ljuskurva: dim vid midnatt, ljus vid lunch, inom intervall, wrap), PlayMode 99/99 (ambient mörkare på natten än mitt på dagen).

## [0.45.0] - 2026-06-22 — Alpha — "Börs-nyheter 📰"

### Added
- **📰 Börs-nyhetshändelser** — vissa börsdagar dyker en rubrik upp som skakar om en enskild aktie:
  positiva ("{bolag} landar rikstäckande kedjeavtal", "viral kläckningsvideo") ger +8–18%, negativa
  ("foderbrist", "myndighetsböter", "återkallelse") ger −8–18%. Rubriken visas i Stocks-appen och priset
  rör sig samma dag. Deterministiskt per dag — håll koll på nyheterna och tajma dina köp/sälj.

### Tested
- EditMode 738/738 (rubriker deterministiska, träffar riktiga aktier, jolt åt rätt håll, inträffar ibland men ej varje dag), PlayMode 98/98.

## [0.44.0] - 2026-06-22 — Alpha — "Reptil-encyklopedi 📖"

### Added
- **📖 Reptil-encyklopedi** — en ny codex-app som listar ALLA arter i databasen med kroppstyp, antal gener
  i genomet och kända morfer (med namn). En riktig in-game uppslagsbok byggd på spelets egen data — bra för
  att lära sig vad som finns att föda upp. Scrollbar, på telefon + dator.

### Tested
- EditMode 736/736, PlayMode 98/98 (appen nåbar + artkatalogen populerad med 50+ arter).

## [0.43.0] - 2026-06-22 — Alpha — "Börs: limit-order 🎯"

### Added
- **🎯 Limit-order på börsen** — lägg stående order som utlöses automatiskt när kursen passerar din nivå:
  auto-köp när priset faller till/under, auto-sälj när det stiger till/över. Order kollas varje börsdag.
  I Stocks-appen: "Limit buy −10%" / "Limit sell +10%"-knappar (lägger order 10% under/över aktuell kurs)
  + visar antal öppna order med en avbryt-knapp. Order sparas mellan sessioner.

### Tested
- EditMode 736/736 (limit buy/sell fyller vid rätt prisnivå, avbryt fungerar, persistens), PlayMode 97/97.

## [0.42.0] - 2026-06-22 — Alpha — "Co-op: ONLINE (TCP) 🌍"

### Added
- **🌍 Co-op spelbart över nätverk (Milstolpe 5/5)** — riktig TCP-transport. Öppna Co-op-appen och välj
  **Host a game** (öppnar port 7777) eller skriv en kompis **IP** och **Join**. Host kör den auktoritativa
  butiken; klienten speglar världen, ser värdens avatar röra sig, och alla handlingar (köp/sälj, aktier,
  bär/släpp) körs på host och speglas tillbaka. Snabbaste testet: kör två spel-instanser och joina
  `127.0.0.1`. LAN funkar via host-datorns lokala IP; internet via port-forward av 7777.
- Trådsäker socket-läsning med main-thread-pump (`CoopPump`) så allt spel-tillstånd ändras på Unitys huvudtråd.

### Notes
- Localhost + LAN funkar direkt. Internet kräver att host port-forwardar 7777 (TCP). NAT punch-through
  (slippa port-forward) kan läggas till senare (UDP/LiteNetLib) bakom samma gränssnitt.

### Tested
- EditMode 733/733, PlayMode 97/97 — inkl. två RIKTIGA sockets över 127.0.0.1: anslutning, meddelanden åt båda håll, full världs-snapshot + ett live köp-kommando över socketen.

## [0.41.1] - 2026-06-22 — Alpha — "Co-op: meny 📋"

### Added
- **📋 Co-op-meny (Milstolpe 5b/5)** — ny **Co-op-app** på datorn: statusrad, "Host a game", ett fält för
  kompisens IP + "Join", och "Leave". Knapparna driver en riktig `CoopController`/`CoopSession` via en
  Core-söm (`ICoopController`); en transport-factory-söm är förberedd där nätverks-socketen pluggas in (M5).
  Tills dess faller host/join tillbaka snyggt med ett tydligt statusmeddelande.

### Tested
- EditMode 733/733, PlayMode 95/95 (controller host/join/leave + status; saknad transport hanteras snyggt; appen nåbar + bygger fönster i ett live-spel).

## [0.41.0] - 2026-06-22 — Alpha — "Co-op: session-fasad 🧩"

### Added
- **🧩 Co-op session-fasad (Milstolpe 5a/5)** — `CoopSession`: en enda enkel ingång för att starta/gå med i
  co-op (StartHost / StartClient / SendLocalAvatar / Stop). Den buntar ihop host-, world-host- och klient-
  delarna bakom ett rollbaserat API, så att den kommande co-op-menyn och den riktiga nätverks-socketen bara
  behöver prata med den här klassen. Transport-agnostisk: loopback i test/editor, riktig socket i skarpt läge.
- Nästa steg mot spelbart: in-game co-op-meny (Host/Join + IP-fält), sedan själva socketen (tillsammans).

### Tested
- EditMode 733/733, PlayMode 92/92 (hel host↔klient-session via fasadens publika API: snapshot, avatar åt båda håll, kommando-routing, ren teardown).

## [0.40.1] - 2026-06-22 — Alpha — "Co-op: world-kommando 🛠"

### Added
- **🛠 Co-op world-kommando (Milstolpe 4b/5)** — en spelares avsikt körs nu mot de RIKTIGA spel-tjänsterna
  på host: när klienten säljer ett djur kör host den kanoniska `SellReptile` (beräknar pris, tar bort djuret,
  krediterar, publicerar event) och speglar resultatet (saldo + borttagning) till klienten. Samma sanning
  för båda spelarna, ingen divergens. Mönstret återanvänds för fler handlingar (placera/flytta) härnäst.

### Tested
- EditMode 733/733, PlayMode 90/90 (klient säljer → host kör SellReptile → host-värld + klient-spegling stämmer: saldo upp, djur borttaget på båda).

## [0.40.0] - 2026-06-22 — Alpha — "Co-op: delat ägarskap 🤝"

### Added
- **🤝 Co-op carry/ägarskap-synk (Milstolpe 4/5)** — host-auktoritativ konflikt-arbitrering så två spelare
  inte kan greppa samma sak samtidigt. När en spelare tar upp ett djur (eller börjar flytta en möbel) äger
  hen det tills hen släpper; den andres försök avvisas av host, och båda ser vem som bär vad. pickUp/drop
  går över kommando-pipelinen och speglas till klienten.
- Nästa (vid live-wiring): koppla placera/flytta/bygg-kommandon till de riktiga World-tjänsterna + visa det
  burna objektet i handen.

### Tested
- EditMode 733/733 (arbiter: grant/återanvänd/avvisa/release; över loopback: klient-pickup beviljas, host blockeras tills släppt, ägarskap speglas). PlayMode opåverkat (isolerad Net-assembly): 89/89.

## [0.39.1] - 2026-06-22 — Alpha — "Co-op: fjärr-avatar 🧍"

### Added
- **🧍 Co-op fjärr-avatar (Milstolpe 3b/5)** — `RemoteAvatarView` driver den andra spelarens kropp i världen
  från den interpolerade nätverks-posen: position, riktning och gå/står-flagga. Rörelsen är jämn tack vare
  interpolatorn. Den synliga riggade modellen (CC0) kopplas på vid live-anslutning; den här delen äger
  rörelsen och är PlayMode-verifierad.

### Tested
- EditMode 729/729, PlayMode 89/89 (Transform följer interpolerad pose: position/rotation/rörelse-flagga; når mål-pose i slutet av fönstret).

## [0.39.0] - 2026-06-22 — Alpha — "Co-op: avatar-sync 🚶"

### Added
- **🚶 Co-op avatar-sync (Milstolpe 3a/5)** — protokollet för att se varandra röra sig: en `AvatarState`
  (position, riktning, går/står) skickas mellan spelarna, och en `AvatarInterpolator` mjukar ut rörelsen
  mellan nätverks-uppdateringarna (linjär interpolation av position + kortaste-väg för riktning) så den
  andra spelaren glider istället för att hoppa. Host och klient skickar varandras pose.
- Nästa steg (M3b): rendera den faktiska avataren i världen från den interpolerade posen.

### Tested
- EditMode 729/729 (interpolation lerpar + clampar + wrap-hanterar yaw; pose når fram åt båda håll över loopback). PlayMode opåverkat (isolerad Net-assembly): 88/88.

## [0.38.0] - 2026-06-22 — Alpha — "Co-op: kommando-pipeline 🔀"

### Added
- **🔀 Co-op kommando-pipeline (Milstolpe 2/5)** — klienten skickar *avsikter* (typade kommandon) som
  **host kör auktoritativt** mot sin värld och broadcastar tillbaka som event; klienten speglar bara den
  ändrade delen (ingen full re-snapshot per handling). Första kommandona: köp/sälj av aktier. Host
  validerar (t.ex. avvisar köp man inte har råd med), så klienten kan aldrig fuska sig till pengar.
- Okända kommandon vidarebefordras till en host-modul (för world-kommandon i kommande milstolpar).

### Tested
- EditMode 725/725 (köp/sälj appliceras host-auktoritativt + speglas; sälj-allt rensar innehav; host avvisar oaffordabla köp). PlayMode opåverkat (isolerad Net-assembly): 88/88.

## [0.37.0] - 2026-06-22 — Alpha — "Co-op: nätverks-kärna 🌐"

### Added
- **🌐 Co-op grundstomme (Milstolpe 1/5)** — första steget mot delad-butik-co-op för 2 spelare. Lagt en
  transport-agnostisk nätverks-kärna: `INetTransport`-söm, en `LoopbackTransport` för in-process-test,
  meddelande-envelope, samt `CoopHost`/`CoopClient` med **snapshot-handskakning** — host serialiserar hela
  spelvärlden (via befintliga save-systemet) och klienten speglar den vid anslutning.
- Host-auktoritativ listen-server-modell (host = spelare + server). Allt byggs + verifieras headless bakom
  loopback; den riktiga socketen (port-forward) kopplas in i en senare milstolpe. Plan: `docs/COOP-PLAN.md`.

### Tested
- EditMode 721/721 (loopback levererar åt båda håll; snapshot speglar pengar/aktier/world; hello→snapshot; host tar emot kommandon), PlayMode 88/88.

## [0.36.0] - 2026-06-22 — Alpha — "Rival-aktier 🏪"

### Added
- **🏪 Rival-prestanda driver aktiekursen** — rival-butikerna (Exotic Scales, Morph Masters, Apex
  Reptiles, Scaled Kingdom, Viper Vault) är noterade som aktier vars kurs nu klättrar extra när
  butiken växer i rykte/försäljning. En blomstrande konkurrent blir en het aktie. Rival-aktier är
  märkta "🏪 rival" i Stocks-appen.

### Tested
- EditMode 717/717 (nudge skalar med score + är capad; växande rival slår passiv rival på samma RNG-seed), PlayMode 88/88.

## [0.35.0] - 2026-06-22 — Alpha — "Börs-djup: utdelning, events, graf 📊"

### Added
- **💰 Utdelningar** — flera bolag delar ut per aktie var 5:e dag (krediteras vid dag-avslut).
- **🐂📉 Marknads-events** — deterministiska bull-/krasch-dagar som tillfälligt förstärker prisrörelsen,
  med en banner i Stocks-appen.
- **📊 Pris-sparkline** — varje aktie visar en liten kursgraf (▁▂▃▅▇) av senaste dagarnas priser; historik
  sparas per aktie.

### Tested
- EditMode 715/715 (event-determinism, utdelnings-matte, historik-cap, save round-trip), PlayMode 88/88 (utdelning krediteras).

## [0.34.0] - 2026-06-21 — Alpha — "Aktiemarknad: kärna 📈"

### Added
- **📈 Aktiemarknad (kärna)** — ny reptil-börs med 8 noterade bolag: rival-butikerna (Exotic Scales,
  Morph Masters, Apex Reptiles, Scaled Kingdom, Viper Vault) + branschbolag (Herp Industries, Cricket
  Foods, Terra Habitats). Deterministisk daglig prisrörelse, köp/sälj av aktier, portfölj med
  genomsnittligt anskaffningsvärde (GAV) + orealiserad vinst/förlust, dagsförändring i %. Ny **Stocks-app**
  (telefon + dator). Innehav + kurser sparas mellan sessioner.
- Första steget av det utbyggda aktiemarknads-systemet; utdelningar, marknads-events och prisgrafer kommer härnäst.

### Tested
- EditMode 712/712 (6 nya börs-tester), PlayMode 88/88 (köp debiterar, daglig tick rör pris, sälj krediterar, app nåbar).

## [0.33.0] - 2026-06-21 — Alpha — "Builders' Market 🏗"

### Added
- **🏗 Builders' Market** (speltestar-feedback #12): en butik (app på telefon + dator) som listar ALLA
  byggbara saker — terrarier, racks och dekor — med pris, fotavtryck och vilken nivå de låses upp på.
  Det är butiks-ytan för bygg-sakerna; placering sker fortfarande via bygg-läget (B). Full borttagning av
  bygg-menyn till förmån för enbart fysiska butiker är en större uppföljning.

### Tested
- PlayMode-test verifierar att storefront listar hela katalogen + är nåbar. EditMode 706/706, PlayMode 87/87.

## [0.32.0] - 2026-06-21 — Alpha — "Djur-upplåsning per storlek 🔒"

### Added
- **🔒 Djur låses upp ihop med terrarie-storleken** (speltestar-feedback): du kan inte längre köpa djur
  vars terrarie-storlek du inte låst upp. Marketplace blockerar köp tills butiksnivån når storlekens tier
  (Small lvl1 · Medium lvl2 · Large lvl4 · XL lvl5) och visar "Locked — reach shop level X".

### Tested
- EditMode 706/706 (ny unlock-helper-test), PlayMode 86/86 (köp blockeras under tier, lyckas vid rätt nivå).

## [0.31.0] - 2026-06-21 — Alpha — "Tom lokal vid start 🧹"

### Changed
- **🧹 Lokalen startar tom** (speltestar-feedback): butiken börjar nu ren — bara datorn/skrivbordet och
  lamporna finns från start. Övrig inomhus-startinredning (soffor, hyllor, växter, mattor, skyltar)
  spawnas inte längre, så du bygger upp butiken själv. (Stadens utomhus-miljö är orörd.)

### Tested
- PlayMode-test verifierar att ambient-inredningen bara innehåller lampor. EditMode 705/705, PlayMode 85/85.

## [0.30.0] - 2026-06-21 — Alpha — "Gula väglinjer 🛣️"

### Added
- **🛣️ US-stil vägar** (speltestar-feedback): varje vägbit har nu en gul mittlinje längs körbanan, så
  stadens gator ser ut som riktiga asfaltsvägar. (Linjen är en tunn primitiv-strip i kod ovanpå de
  befintliga CC0-vägbitarna.)

### Tested
- PlayMode-test verifierar att gula mittlinjer (road_line) byggs i staden. EditMode 705/705, PlayMode 84/84.

## [0.29.0] - 2026-06-21 — Alpha — "Render distance 🔭"

### Added
- **🔭 Render distance-inställning** (speltestar-feedback): välj Low/Medium/High/Ultra i Settings-appen —
  sätter huvudkamerans far clip plane (150/300/600/1200) så du kan balansera sikt mot prestanda. Valet
  sparas och återställs vid load.

### Tested
- EditMode 705/705 (4 nya tester), PlayMode 84/84 (kamerans farClipPlane följer vald tier).

## [0.28.0] - 2026-06-21 — Alpha — "Telefon-scroll 📱"

### Fixed
- **📱 Telefonens app-skärm scrollar** (speltestar-feedback): med 18 appar spillde ikonerna utanför
  telefonskärmen. Hemskärmen har nu en scrollbar ikon-grid så alla registrerade appar får plats och
  stannar på telefonen.

### Tested
- PlayMode-test verifierar att antal hemskärms-ikoner = antal registrerade appar (alla syns). EditMode 701/701, PlayMode 83/83.

## [0.27.0] - 2026-06-21 — Alpha — "Flytta möbler tydligare 🪑"

### Changed
- **🪑 Flytta möbler** (speltestar-feedback): att flytta redan placerade möbler fanns redan (välj möbel i
  bygg-läget → Move), men var svårt att hitta. Fixtur-panelen har nu en tydlig instruktion ("Aim at a new
  spot, then press Move…") och knappen heter "Move here". Flytt-logiken (frigör gamla celler, behåller
  djur/index, ingen återbetalning) är oförändrad och täckt av tester.

### Tested
- EditMode 701/701 (Move-tester gröna), PlayMode 83/83.

## [0.26.0] - 2026-06-21 — Alpha — "Storlek i Marketplace 📐"

### Added
- **📐 Nödvändig terrarie-storlek per reptil i Marketplace** (speltestar-feedback): varje listning visar
  nu vilken terrarie-storlek djuret behöver som vuxen (Small/Medium/Large/XLarge) — både på kortet
  ("Needs: …") och i detalj-panelen — så du kan planera boendet innan du köper.

### Tested
- EditMode 701/701 (ny format-test), PlayMode 83/83.

## [0.25.0] - 2026-06-21 — Alpha — "Day speed ⏩"

### Added
- **⏩ Day-speed control** (speltestar-feedback): välj hur snabbt dagen går — **x1/x2/x3** — i den nya
  **Settings-appen** (telefon + dator). x1 ≈ ~20 min/dag; x2/x3 proportionellt snabbare. Valet skalar
  tick-takten direkt och sparas mellan sessioner. (Settings-appen är på engelska — start på UI-engelska-passet.)

### Tested
- EditMode 700/700 (4 nya tester), PlayMode 83/83 (Settings → tick-speed skalas + app nåbar).

## [0.24.0] - 2026-06-21 — Alpha — "Grön bygg-markering 🟩"

### Added
- **🟩 Vald sak i bygg-menyn blir grön** (speltestar-feedback): det valda objektet i bygg-katalogen
  markeras nu med grön bakgrund + grön ram, så du tydligt ser vad som är aktivt.

### Tested
- PlayMode-test verifierar att vald rad är grön-dominant. EditMode 696/696, PlayMode 82/82.

## [0.23.0] - 2026-06-21 — Alpha — "Placerings-bock 🎯"

### Added
- **🎯 Grön bock vid crosshairet** (speltestar-feedback): när du håller ett djur och siktar på ett
  terrarium/rack med ledig plats visas en liten grön ✓ bredvid crosshairet — så du ser direkt att det
  går att placera där (försvinner om behållaren är full eller du inte siktar på något giltigt).

### Tested
- PlayMode-test verifierar HUD→crosshair-seamen. EditMode 696/696, PlayMode 81/81.

## [0.22.0] - 2026-06-21 — Alpha — "Hoppa 🦘"

### Added
- **🦘 Hoppa med mellanslag** (speltestar-feedback): first-person-spelaren kan nu hoppa med Space när
  hen står på marken.

### Tested
- PlayMode-test verifierar jump-inputens livscykel. EditMode 696/696, PlayMode 80/80.

## [0.21.0] - 2026-06-21 — Alpha — "Auktionshus 🔨"

### Added
- **🔨 Auktionshus**: lägg ut ett ägt djur på auktion — det avgörs efter ett par dagar till ett
  premiumpris (1,30–1,60× marknadsvärde), pengarna sätts in och djuret lämnar samlingen. Ny
  **Auktionshus-app** (telefon + dator) för att lista djur + se pågående auktioner. Sparas.

### Tested
- EditMode 696/696 (4 nya auktions-tester), PlayMode 79/79 (lista → avgörs på dag-avslut → premie + djur borta).

## [0.20.0] - 2026-06-21 — Alpha — "Stadsbelysning 💡"

### Added
- **💡 Gatlykts-belysning**: gatlyktorna närmast butiken kastar nu ett varmt sken så kvarteren glöder
  på kvällen. Antalet realtidsljus är kapat (18) för prestanda. Kod-driven (Light-komponenter på de
  befintliga lykt-modellerna) — ingen egen 3D.

### Tested
- PlayMode-test verifierar att lyktor har ljus och att antalet är kapat. EditMode 692/692, PlayMode 78/78.

## [0.19.0] - 2026-06-21 — Alpha — "Tätare stad 🏙️"

### Changed
- **🏙️ Mycket tätare & livligare stad**: kvartersrutnätet utökat från 13×13 till 17×17 — fler byggnader
  och skyskrapor, fler träd & gatlyktor, fler bilar och fotgängare på gatorna, och vägnätet täcker hela
  den större kartan. Allt med redan nedladdade CC0-modeller (ingen egen 3D).

### Tested
- PlayMode-test verifierar >120 byggnader i staden. EditMode 692/692, PlayMode 78/78.

## [0.18.0] - 2026-06-21 — Alpha — "Marknadstrender 📈"

### Added
- **📈 Marknadstrender**: marknaden svänger varje dag (±0–20%) och **skalar dina faktiska
  försäljningspriser** — både visat begärt pris och utbetalning följer trenden. Ny **Marknad-app**
  (telefon + dator) visar dagens trend + några dagars utsikt, så du kan tajma försäljningar.

### Tested
- EditMode 692/692 (4 nya trend-tester), PlayMode 78/78 (ComputeSalePrice följer trenden + app nåbar).

## [0.17.0] - 2026-06-21 — Alpha — "Sparkonto 💰"

### Added
- **💰 Sparkonto** i banken: sätt in pengar och tjäna **1% ränta per dygn** (lägre än lånets 2%). Sätt
  in/ta ut via Bank-appen; balansen växer vid dag-avslut och sparas mellan sessioner. Ger en plats att
  parkera överskott och en mjuk ekonomisk progression.

### Tested
- EditMode 688/688 (4 nya sparkonto-tester inkl. save round-trip), PlayMode 77/77 (insättning → ränta → uttag).

## [0.16.0] - 2026-06-21 — Alpha — "Samarbeten 🤝"

### Added
- **🤝 Samarbeten / co-op-kontrakt**: NPC-uppfödare (Morph Masters, Apex Reptiles, stadens zoo m.fl.)
  erbjuder order — leverera djur (genom att sälja) för kontant-belöning + ryktesbonus. Klarade kontrakt
  roteras automatiskt mot nya. Ny **Samarbeten-app** (telefon + dator) med progress + claim. Sparas.
- Ännu en offline-grund för framtida online-co-op (samma modell kan matas av riktiga medspelare).

### Tested
- EditMode 684/684 (5 nya kontrakt-tester inkl. save round-trip), PlayMode 77/77 (leverans → claim + app).

## [0.15.0] - 2026-06-21 — Alpha — "Konkurrenter & topplista 🏆"

### Added
- **🏆 Konkurrenter + topplista** (co-op/konkurrens, offline): fem AI-rivalbutiker (Exotic Scales,
  Morph Masters, Apex Reptiles m.fl.) tävlar mot dig — de växer i rykte och försäljning varje dag, och en
  ny **Topplista-app** (telefon + dator) rankar dig mot dem efter en kombinerad poäng med din rad
  markerad. Rivalerna sparas mellan sessioner.
- Grunden för framtida online-co-op: samma modell kan senare matas av riktiga nätverksspelare.

### Tested
- EditMode 679/679 (5 nya konkurrent-tester inkl. save round-trip), PlayMode 76/76 (rivaler växer + ranking + app).

## [0.14.0] - 2026-06-21 — Alpha — "Bank & lån 🏦"

### Added
- **🏦 Bank/lån**: låna kapital upp till en kreditgräns som skalas med rykte och butiksnivå. Skulden
  får 2% ränta per dygn och återbetalas valfritt belopp i den nya **Bank-appen** (telefon + dator).
  Skulden sparas mellan sessioner.

### Tested
- EditMode 674/674 (5 nya lån-tester inkl. save round-trip), PlayMode 75/75 (lån → ränta → återbetala + app).

## [0.13.0] - 2026-06-21 — Alpha — "Nyheter 📰"

### Added
- **📰 Nyheter-app** (telefon + dator): en in-game-feed med höjdpunkterna från varje uppdatering, så
  spelaren ser vad som är nytt utan att lämna spelet.

### Tested
- EditMode 669/669 (ny news-modelltest), PlayMode 74/74 (app nåbar + listar poster).

## [0.12.0] - 2026-06-21 — Alpha — "Dagens uppdrag 🎯"

### Added
- **🎯 Dagliga mål/uppdrag**: varje speldag har ett mål (sälj X djur / tjäna $Y / kläck Z djur) som
  spåras automatiskt och ger en kontant-belöning när det är klart. Ny **Dagens uppdrag-app**
  (telefon + dator) visar mål, framsteg och en hämta-belöning-knapp. Mål + framsteg sparas.

### Tested
- EditMode 668/668 (5 nya mål-tester inkl. save round-trip), PlayMode 73/73 (progress → claim → belöning + app).

## [0.11.0] - 2026-06-21 — Alpha — "Statistik & rekord 📊"

### Added
- **📊 Statistik-/rekordtavla** (roadmap leaderboard, single-player): livstidsstatistik som räknas upp
  löpande — totalt sålda djur, total försäljningsintäkt, bästa enskilda försäljning, totalt uppfödda —
  plus dag, kassa, rykte, antal djur/filialer/anställda. Ny **Statistik-app** (telefon + dator). Sparas.

### Tested
- EditMode 663/663 (ny persistens-test), PlayMode 72/72 (events → räknare + app nåbar).

## [0.10.0] - 2026-06-21 — Alpha — "Utomhushägn 🌿"

### Added
- **🌿 Utomhushägn (Outdoor Habitat)** (roadmap outdoor enclosures): en ny, största terrarie-tier — 6×5
  fotavtryck, 6 djurplatser, bioaktiv utrustning, räknas som XLarge så även de största arterna får plats.
  Köps i bygg-läget som övriga terrarier.

### Tested
- EditMode 662/662 (katalog- + sizing- + alias-tester täcker den nya tiern), PlayMode 71/71.

## [0.9.0] - 2026-06-21 — Alpha — "Butikstema 🎨"

### Added
- **🎨 Butiks-teman** (roadmap custom shop themes): välj färgtema för butiken — Klassisk ek, Modern grå,
  Djungel, Öken eller Nattmarknad. Temat färgar om golv/väggar/tak direkt och sparas mellan sessioner.
  Ny **Butikstema-app** (telefon + dator) med färgrutor + "Välj".

### Tested
- EditMode 662/662 (4 nya tema-tester), PlayMode 71/71 (väggmaterial får temats färg + app nåbar).

## [0.8.0] - 2026-06-21 — Alpha — "Personal-kompetens 📈"

### Added
- **📈 Anställda-djup** (roadmap 0.8): varje anställd har nu en **kompetensnivå (1-5)** som går att
  **uppgradera** (kostar, höjer lönen) i Personal-appen. Högre nivå = mer uträttat: **skötare på nivå 2+
  behandlar även sjuka djur** (in-house vet), och **säljare listar djur med ett påslag** som växer med
  nivån. Nivåer sparas mellan sessioner (bakåtkompatibelt: gamla anställda blir nivå 1).

### Tested
- EditMode 658/658 (5 nya nivå-tester inkl. save round-trip), PlayMode 70/70 (uppgradera → påslag + lön).

## [0.7.0] - 2026-06-21 — Alpha — "Filialer 🏬"

### Added
- **🏬 Filialer / karta & stad** (roadmap 0.7): hyr butikslokaler runt om i staden (Förortskiosken,
  Köpcentret, Citybutiken). Varje filial ger en passiv daglig nettointäkt som skalas med ditt rykte
  (känt varumärke → mer kundström) minus hyra, som dras/läggs vid dag-avslut. Ny **Filialer-app**
  (telefon + dator) för att hyra/säga upp och se netto. Filialer sparas mellan sessioner.

### Tested
- EditMode 653/653 (5 nya branch-tester inkl. save round-trip), PlayMode 70/70 (hyr → daglig netto → app).

## [0.6.0] - 2026-06-21 — Alpha — "Recensioner ⭐"

### Added
- **⭐ Kundrecensioner & rykte** (roadmap 0.6 marknadsföring/trafik): varje försäljning ger en
  recension vars betyg speglar hur välskötta butikens djur är (snitt-wellbeing). Snittbetyget puttar
  ryktet upp/ned per dygn — välskötta djur → bra recensioner → högre rykte → fler kunder. Ny
  **Recensioner-app** (telefon + dator) med snittbetyg + senaste omdömen. Recensioner sparas.

### Tested
- EditMode 648/648 (5 nya review-tester inkl. save round-trip), PlayMode 69/69 (sälj → recension → rykte → app).

## [0.5.0] - 2026-06-20 — Alpha — "Ömsning 🌀"

### Added
- **🌀 Ömsnings-cykel (shed)** (roadmap 0.5 djup husbandry): djur går regelbundet in i ömsning under
  några dagar. Hålls de väl vattnade blir ömsningen ren — annars blir det en "stuck shed" som drar ner
  hälsan. Cykeln drivs ett steg per speldag och visas i terrariets Djur-flik ("🌀 Ömsar — X dagar kvar").
  Ömsnings-status sparas mellan sessioner.
- Bygger ovanpå befintlig sjukdom + vet-behandling (CareAction.Treat) → en rikare skötsel-loop.

### Tested
- EditMode 643/643 (5 nya shed-tester inkl. save round-trip), PlayMode 68/68 (cykel-advance på dag-avslut).

## [0.4.0] - 2026-06-20 — Alpha — "Anställda 👤"

### Added
- **👤 Anställda-system** (roadmap 0.8-tema): anlita **Skötare** (matar/vattnar/städar alla djur
  automatiskt varje dag) och **Säljare** (lägger automatiskt ut djur till försäljning). Lön dras varje
  dygn vid dag-avslut. Ny **Personal-app** (telefon + dator) för att anlita/avskeda och se lönekostnad.
  Anställda sparas mellan sessioner.

### Notes
- Första minor-bumpen (0.3 → 0.4): minor får nu klättra fritt (0.4, 0.5 …) medan major stannar på 0.

### Tested
- EditMode 638/638 (5 nya modell/persistens-tester), PlayMode 67/67 (anlita → dag-arbete + lön + app).

## [0.3.63] - 2026-06-20 — Alpha — "Marknadsföring 📣"

### Added
- **📣 Marknadsförings-system** (roadmap): köp annonskampanjer (flygblad/lokaltidning/sociala medier)
  som **drar fler kunder till butiken** under ett antal dagar. Ny **Marknadsföring-app** (telefon + dator)
  visar aktiv kampanj + dagar kvar; kampanjen räknas ner en dag per dygn och sparas mellan sessioner.

### Tested
- EditMode 633/633 (6 nya modell-tester), PlayMode 66/66 (full wiring: köp → trafik-boost → nedräkning → app).

## [0.3.62] - 2026-06-20 — Alpha — "Utmärkelser 🏆"

### Added
- **🏆 Achievements-system** (roadmap): 10 utmärkelser som låses upp av spelandet — första
  försäljningen, 10 sålda, första kläckningen, 25 uppfödda, $5k/$50k, 100 rykte, 10 djur, 5 arter,
  butiksnivå 3. Visas i en ny **Utmärkelser-app** (telefon + dator); sparas mellan sessioner.

### Tested
- PlayMode-test verifierar att utmärkelser delas ut på events + att appen är nåbar. EditMode 627/627, PlayMode 65/65.

## [0.3.61] - 2026-06-20 — Alpha — "Kläck ägg var som helst 🥚"

### Added
- **🥚 Ägg & kläckning-app** på både telefonen (tryck **P**) och datorn: listar alla ägg som ruvas
  (art, antal, dagar kvar) med en **"Hatcha nu"-knapp** som kläcker ägget direkt — så du kan kläcka
  ägg var som helst, inte bara vid en breeding rack.

### Tested
- PlayMode-test verifierar att appen är registrerad/nåbar och listar ägg. EditMode 627/627, PlayMode 64/64.

## [0.3.60] - 2026-06-20 — Alpha — "Tydligare dekor-köp"

### Changed
- **🪴 Dekoration-köpknappen** visar nu både kvalitetsbonusen och kostnaden för nästa nivå
  ("Köp nästa nivå (+5% kvalitet · $150)").

### Tested
- EditMode 627/627, PlayMode 63/63.

## [0.3.59] - 2026-06-20 — Alpha — "Tillbaka till djurlistan ↩️"

### Changed
- **↩️ "Tillbaka" i Skötsel-fliken** går nu till djurlistan istället för att stänga hela panelen —
  smidigare att hoppa mellan djur. (Stäng panelen med ✕ eller E/Esc som vanligt.)

### Tested
- PlayMode-test verifierar att Back återgår till Djur-fliken utan att stänga panelen. EditMode 627/627, PlayMode 63/63.

## [0.3.58] - 2026-06-20 — Alpha — "Klicka för att sköta 👆"

### Added
- **👆 Klickbara djur-rader.** Klicka på ett djur i Djur-fliken för att välja det och hoppa direkt
  till Skötsel-fliken för just det djuret — smidigt i terrarier med flera djur.

### Tested
- PlayMode-test verifierar att val + flikbyte sker. EditMode 627/627, PlayMode 63/63.

## [0.3.57] - 2026-06-20 — Alpha — "Trångbodd-varning i översikten ⚠️"

### Added
- **⚠️ Antal trångbodda djur** visas nu i Djur-flikens summering, så du snabbt ser om något djur
  behöver ett större terrarium.

### Tested
- EditMode 627/627, PlayMode 63/63.

## [0.3.56] - 2026-06-20 — Alpha — "Terrariets totalvärde 💎"

### Added
- **💎 Totalt marknadsvärde** för djuren visas nu i Djur-flikens summering, så du ser terrariets
  samlade värde direkt.

### Tested
- EditMode 627/627, PlayMode 63/63.

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
