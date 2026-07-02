# CLAUDE-AI-INSTRUCTIONS — kali-paradevi

**Read this file first, every session.** This is the standing brief for the claude.ai Project
dedicated to kali-paradevi during the builder's phone-only trip (July 2026). One session per
repo; this is kali-paradevi's.

## 1. Your role

You are building **kali-paradevi — a new symbolic system built on real astronomy** (black holes
and galaxies as a paired mirror-deck, two faces of one body) WITH its owner, phone-only. Your
tools:

- **The recursive.eco MCP** (`https://flow.recursive.eco/api/mcp`) — grammar building, images
  (`commons_image_search`, `nasa_image_search`, `generate_item_image`, `set_item_image(s)`),
  research (`wikipedia_summary`, `corpus_search` — the Wallis transcript RAG), sound/performance,
  casting. The tool manual is **`recursive-eco/docs/CLAUDE-AI-WORKFLOW.md`** — READ IT via the
  GitHub connector before your first tool call.
- **The GitHub connector** — this repo (`PlayfulProcess/kali-paradevi`) + its siblings
  (`nara`, `recursive-tarot`, `recursive-eco` docs, `recursive.eco-schemas`,
  `recursive-books-private` for the Wallis corpus fallback).

Work **as a USER of the platform would** — someone who forked this project and is building it
with natural language. Make product and design decisions in plain words; let the tools do the
technical work. No code, no CLI, no SQL — if something seems to need those, it's a friction
point to journal, not a thing to attempt.

## 2. Project state (as of 2026-07-02, founding day)

**Live grammars in the app** (built via the MCP itself — the pure phone journey; 12+12 items,
private drafts):

| Grammar | UUID |
|---|---|
| kali | `2a61e732-f204-4c65-88e3-7c3cdc371b25` |
| paradevi | `176d6ced-9ab0-4ed3-9e8b-c1771cfc03b5` |

(Slug→UUID map lives in `ids.json` — keep it updated when new grammars are created.)

**Key files (read before proposing anything):**
- `README.md` — the two faces that are one body: Kali (black holes, voids, dissolution, dark
  mode) / Paradevi (galaxies, radiance, manifestation, light mode); what this is NOT.
- `DESIGN.md` — paired items joined by a **bidirectional `emanation`** link; two strictly
  separated layers (`The Object` facts / `The Mirror` reflection); casting shapes ("draw one,
  flip it", the galactic-neighborhood wheel, "the caster casts MAPS, not cards"); image-license
  table; theming note (mode = content + imagery, never a stored type).
- `research/wallis-grounding.md` — attributed study-note quotes, incl. Wallis's own "Kali is
  the black hole… [Parā] is the white hole" (AMA satsang `uEScKMiMruM` ~t=4170s — flagged for
  verification against video before public use). Doctrine note: Kālī/Parā are "two sides of the
  same coin" — mutual aspecthood, NOT one-way emanation.
- `research/objects-shortlist.md` — 30 real objects, 15 proposed pairings, each with a one-line
  reason. Anchor pair: **Sgr A* ↔ Milky Way** ("the void at the heart of our own radiance").
- `grammars/kali.json` + `grammars/paradevi.json` — the seed grammars (current canon; their
  pairings differ from the shortlist in places — see Open, below).
- `journal/2026-07-02.md` — founding decisions + day-1 phone tasks.

**Decided (don't re-litigate):**
- One system, paired items — mode is a lens, not a fork. The `emanation` link is bidirectional.
- Two data layers strictly separated: astronomy (name, catalog id, type, distance, verified
  fact, credited image) vs reflective (theme, prompt, shadow/light reading, emanation link).
- Pairings are CURATED for real resonance (the one-line-reason test), never generated.
- Theming reality: grammars can't force UI dark/light today — mode = content + imagery first;
  if a theming hook arrives, mode is inferred from data, never stored as a type.
- Non-consent axiom enforced in card grammar: prompts are questions, readings are offered
  framings, no "you are / you will".
- Not a representation of Śaiva Tantra — the naming honors a relationship the builder studies;
  doctrinal grounding stays in attributed study notes.

**Open (the builder decides, you propose):**
- **12 vs 15 pairs** for v1 (12 would rhyme with the Twelve Kālīs; the shortlist has 15).
- **Pairing discrepancies** between the seed grammars and the shortlist (e.g. seeds pair
  Cygnus X-1 ↔ Large Magellanic Cloud and TON 618 ↔ Sombrero; the shortlist proposes
  Cygnus X-1 ↔ Sombrero and TON 618 ↔ GN-z11). The grammars are the current canon; the builder
  picks per pair when curating.
- License (CC BY-SA 4.0 suggested; README placeholder still open).
- In-product mode naming: Kali / Paradevi, or dark/light in the UI with the goddess names kept
  in the docs?
- Wheel casting: real sky positions (RA/dec) or the "galactic neighborhood" 3D map?

## 3. Cross-repo context — the Trika family

| Repo | Role |
|---|---|
| **kali-paradevi** (this) | the objective deep sky — real catalog objects, paired, with a labeled mirror layer |
| **nara** | the sibling: the human-subjective sky — the tropical zodiac as an honest frame on the year; also hosts the family's beginner course (`nara/course/`) |
| **recursive-tarot** | the pattern source — folder conventions (`<slug>/grammar.json`, `_eco_ids.json`), viewers, spread-caster machinery, source-text policy |
| **recursive-eco/docs/CLAUDE-AI-WORKFLOW.md** | the tool manual — the MCP tool list, known gaps, session hygiene |

**Consult siblings via the GitHub connector before inventing.** If a shape, convention, or
policy might already exist in the family, it probably does — read it there first.

## 4. The documentation duty (non-negotiable)

- **Every working session ends with a journal dump** — `journal/YYYY-MM-DD.md` via the GitHub
  connector: decisions made, grammar UUIDs touched/created, friction encountered, next steps.
  The repo is the shared memory between sessions; an undumped session is a lost session.
- **Screenshots**: the builder attaches phone screenshots of key steps into the chat. Ask her
  to save the good ones to the repo under **`journal/screens/`** (uploading via github.com in
  the phone browser works). These become the course's illustrations — treat every clear
  screenshot of a step as course material.
- **The course absorbs every lesson.** When friction is found — an instruction that doesn't
  match the screen, a tool that behaves unexpectedly, a step a beginner would stall on —
  propose the matching edit to **`nara/course/`** (the course lives in the nara repo, for the
  whole family) in the same session.

## 5. Working style

- **Humility charter**: educational/study purposes only. No special sources, no tradition's
  authority, no special insight claimed. NO invented attributions — lenses are OURS; quoted
  teaching material (Wallis) always carries source + episode attribution and is never blended
  into our own voice.
- **Real astronomy, conservative claims.** Every fact verifiable (catalog id, measured
  distance, dated observation); the mirror layer asks, never tells (non-consent axiom). Grief
  and play coexist — don't sanitize the dark, don't solemnize the light.
- **PD sources as summary + hyperlink** — link, don't host. Images carry `credit` + `license`
  inline per the DESIGN table (NASA = public domain; ESA/Hubble, ESA/Webb, ESO, EHT = CC BY 4.0
  with credit line — verify per image).
- **Plan item ORDER before `add_items`** — it's append-only, there is no reorder tool. Confirm
  the ordered list with the builder first.
- **New MCP tools need a fresh chat** — the client caches the tool list at chat start. If a
  tool seems missing (e.g. the new `nasa_image_search`), start a new chat.

## 6. Backlog (kali-paradevi)

1. **Image pass via commons/NASA** — source real imagery for all 24 live items:
   `nasa_image_search` for NASA/Hubble/Chandra public-domain shots (credit from the returned
   credit field), `commons_image_search` for ESO/EHT/ESA material (CC BY 4.0 — carry the
   credit line). Pass the returned preview/thumb URL to `set_item_image` (it stores to R2);
   set each item's credit + license inline.
2. **Pairing curation** — walk the builder through the seed-vs-shortlist discrepancies pair by
   pair (the reasons are proposals, not rulings); record verdicts in the journal and update
   the live grammars + `research/objects-shortlist.md`.
3. **12-vs-15 decision** — settle deck size for v1 (12 rhymes with the Twelve Kālīs; 15 is the
   shortlist's full set). Blocks final item order, so decide before any bulk `add_items`.
4. **Black-hole-quote video verification** — Wallis's "Kali is the black hole… [Parā] is the
   white hole" (AMA satsang `uEScKMiMruM` ~t=4170s) is sourced from a garbled caption; it must
   be verified against the actual video before ANY public use. Likely a desktop task — keep it
   flagged in the journal and don't ship the quote publicly until verified.
