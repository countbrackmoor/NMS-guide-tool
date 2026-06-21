# Changelog — NMS Traveller's Codex

No Man's Sky fan reference. Repo: `countbrackmoor/NMS-guide-tool`. Deployed at `gorgon.live/NMS-guide-tool/`.

The early build history of this project predates this changelog — exact dates and feature order for the first guides aren't reliably recorded. Entries marked "earlier" describe state at a point I have evidence for, not the original commit.

---

## 2026-06-21 — Changelog established

### Added
- This CHANGELOG.md, reconstructed from past work sessions
- Project rule: future changes to this module must be logged here in the same session they're made

---

## ~2026-06-02 — Visual identity pass + seventh guide

### Added
- **Manual VII: Base Construction & Engineering** — full new guide module
  - Teal/emerald `#10b981` with blueprint grid texture
  - Chakra Petch / IBM Plex Mono fonts
  - 10 sections covering power systems, extraction, wiring/logic gates, specialist builds, pro tips
  - Detailed Power Inverter explanation (green/red/control ports, NAND gate logic, automatic door opener circuit example)
- Seventh card on the NMS hub for Base Construction & Engineering

### Changed (visual redesigns)
- **Multi-Tools guide** → deep violet/purple; Orbitron / Share Tech Mono; horizontal scanlines; frequency bar graph watermark
- **Exocrafts guide** → originally restyled to amber/orange (Teko / Roboto Mono, terrain hatching), then **rejected for color conflict with Freighters** and redone in dark blue `#3b82f6` with a circuit grid texture
- NMS hub card colors updated to match new guide identities (violet for Multi-Tools, blue for Exocrafts)

### Changed (hub copy and tags)
- Freighters card title: "Admiral's Command Manual" → "Freighter Command Manual"
- Card tag updated: "Base Building" → "Freighter Base Building"
- "Combat" topic tag removed

### Added (images)
- Card images for all seven modules (`settlements`, `freighters`, `trading`, `ships`, `multitools`, `exocrafts`, `base-building`)
- Background removal on `ships.png` using brightness/saturation masking
- Checkerboard-baked images handled via `mix-blend-mode: lighten` rather than pixel editing
- Settlement and Base Building card images swapped

### Removed
- `.back-link` CSS block

### Changed (nav)
- nav.js added to NMS hub (`nms.html` / `index.html`) only — **not** on individual guide pages, which have their own hub-nav elements that would conflict

### Changed (hero / titles — for No Man's Sky prominence)
- Hub `<title>`: "No Man's Sky — Traveller's Codex" → "No Man's Sky — Traveller's Codex · Fan Guide"
- Eyebrow: → "No Man's Sky · Fan Guide Collection"
- Subtitle: → "A No Man's Sky Field Reference — Beacon & Voyagers Era"
- Hero description rewritten to lead with "A fan-made reference for **No Man's Sky**"

### Fixed (NMS hub structure)
- `nms.html` renamed to `index.html` for repo-root serving
- `<base href="/NMS-guide-tool/">` tag set; all relative hrefs (`index.html`, `nms-*-guide.html`) verified to resolve correctly under it
- Back link `../` resolves to `gorgon.live/`
- Favicon paths absolute: `/favicon.png`, `/favicon-32.png`

### Fixed (accuracy sweep across all guides)
- Removed the entire animated price ticker from the Trading guide (HTML + CSS)
- Replaced per-unit prices throughout with value tier descriptors (Extremely High / Very High / High / Medium / Low–Medium / Good / Variable)
- Trading tables renamed: "Approx Value" → "Value Tier"; "Income/Hour" → "Income Level"
- Recipe value tags re-described: `~1.4M` → "High value"; `~5.5M` → "Very high value"; `~15.6M` → "Extremely high value"
- Sell/keep table reasons stripped of price figures
- Nanite sources table: removed specific hourly figures (30K/hr, 40K/hr, 4,750/planet, 500–5,000/run)
- Trade loop descriptions: removed income figures (1–5M/hr, 75–150M per batch)
- Activated Indium note: removed "165/u" and "949/u"; replaced with contextual language about the nerf
- **Frigate Fuel recipe corrected**: Di-hydrogen only (7× → 50 Tonnes); the Tritium reference removed from recipe list and Fuel Warning callout
- **Iteration: Cronus → Iteration: Hyperion (Synthesis Laboratory)** as the blueprint vendor on the Space Anomaly (Cronus is the food NPC)
- Final grep sweep across all five files confirmed zero remaining error phrases

---

## Earlier — Baseline (pre-changelog)

State that existed before the entries above:

- Multi-repo deployment: `countbrackmoor.github.io` (landing page) + `NMS-guide-tool` (the guides)
- Hub page ("Traveller's Codex") with hero, eyebrow, subtitle, and project cards per guide
- Six guide modules covering Settlements, Freighters & Frigates, Trading & Crafting, and Ships, plus the Multi-Tools and Exocrafts guides that were later redesigned
- Each guide built as a distinct HTML file with its own color and typographic identity
- Filename convention: `nms-[topic]-guide.html`
- Back-to-hub links from each guide

No reliable dated record of when each of these first shipped.
