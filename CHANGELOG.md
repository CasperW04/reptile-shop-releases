# Changelog

Alla noterbara ändringar i **Reptile Shop** dokumenteras här.
Formatet baseras på [Keep a Changelog](https://keepachangelog.com/) och versionerna
följer [Semantic Versioning](https://semver.org/lang/sv/) (MAJOR.MINOR.PATCH).

Detta är samma changelog som visas i spelets huvudmeny och som auto-updatern
hämtar från release-kanalen (`CasperW04/reptile-shop-releases`).

## [Unreleased]

### Planerat (nästa version — se `docs/3D-SHOP-PLAN.md`)
- **Förstaperson + fysisk butik:** gå runt i butiken och placera ut hyllor,
  terrarier och inredning själv (i stil med TCG Card Shop Simulator).
- **Huvudmeny:** New Game / Continue / Load / Settings / Quit + changelog-panel.
- **Sparfiler/slots:** flera namngivna sparfiler, ladda/radera/kopiera.
- **Auto-update i appen:** spelet kollar GitHub Releases vid start, ser om en
  nyare version finns och kan ladda ner + installera den själv.
- Kund-NPC:er med NavMesh, kassa, leveranslådor och daglig öppna/stäng-loop.
- Blender-genererade assets för miljö och inredning.

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

[Unreleased]: https://github.com/CasperW04/reptile-shop/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/CasperW04/reptile-shop/releases/tag/v0.1.0
