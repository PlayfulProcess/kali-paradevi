# Kali · Paradevi — build plan

*The objective sky: black holes + galaxies as a paired mirror-deck. Part of the Trika family on
recursive.eco (sibling: [nara](https://github.com/PlayfulProcess/nara), the subjective sky).*

## What this repo is

A **github-first grammar channel**: the repo is canonical, recursive.eco is the live viewer/app.
Same pattern as `recursive-tarot` and `nara`.

```
recursive-eco.json          channel manifest recursive.eco imports (identity + where grammars live)
ids.json                    slug → recursive.eco UUID map (+ _public_now, _preview_links)
grammars/<slug>/grammar.json  the decks — canonical here, synced to the app
  ├─ kali/       the dark face — black holes, voids (each item names its light twin)
  └─ paradevi/   the light face — galaxies, first light (each item names its dark twin)
docs/                       the PUBLIC WEBSITE (GitHub Pages serves main/docs)
  ├─ index.html   the site: nav · two-faces orb hero · live grammar gallery · how-to-read · Trika
  ├─ ids.json     copy of the root ids.json so the gallery's same-origin fetch works from /docs
  └─ .nojekyll    serve files as-is (no Jekyll)
reference/schemas/          read-only grammar copies for in-repo claude.ai work (trip env blocks cross-repo)
ICONS.md                    SVG-only icon convention + raw paths (never emoji)
```

**Live site:** https://playfulprocess.github.io/kali-paradevi/ (Pages source = `main` / `/docs`).
**Channel on the app:** slug `kali-paradevi`, `source_of_truth: repo`.

## ✅ Done (Jul 3 2026)

- **Real website at `docs/index.html`** — sticky nav (SVG glyph, never emoji), the split-orb "two
  faces" hero, a **live grammar gallery** (fetches `docs/ids.json`, auto-updates as grammars are
  added) with Play / Cards / Study links per grammar, a "how to read" section (the paired void↔radiance
  mechanic + not-predictive charter), and the Trika map. Verified rendering locally.
- **Pages wiring fixed** — the served page is now the real site (Pages source is `/docs`, which the
  earlier root `index.html` never reached); added `docs/.nojekyll` to clear the errored Pages build;
  removed the superseded root `index.html`.
- **Channel manifest wired** — `landing_url` → the Pages site; `icon` set to `null` (the app hero now
  renders an SVG by slug, so no emoji).
- **Two seed grammars public** — `kali` + `paradevi`, paired 1:1 via `metadata.emanation`.

## ▢ Next (roadmap)

1. **Item images from NASA / public domain** *(great phone task on the trip via the recursive.eco
   MCP — `commons_image_search` / a NASA image search).* Both grammars ship with `image_url`
   intentionally absent; add real black-hole / galaxy imagery (Sgr A*, M87*/Pōwehi, Andromeda, the
   Milky Way…). Drop the returned image onto each item; the cards + gallery light up automatically.
2. **Grow the paired deck** — more object pairs (each Kali item still names its Paradevi twin and
   vice-versa). Keep the 1:1 emanation invariant.
3. **A galaxy/black-hole visual on the home page** — an inline SVG or a single hero image once #1 has
   art, so the site shows a real object, not only orbs.
4. **Standalone in-repo card viewer — deferred, probably skip.** The family decision (see
   `nara/library/README.md`) is that the in-app viewers already render every grammar with zero
   hosting; the Play/Cards/Study links do this today. Only build a repo-hosted viewer if we want the
   deck fully browsable without leaving the Pages site.
5. **Custom domain** — optional; point one at the Pages site when chosen (`docs/CNAME` + repo setting).

## Invariants (don't break)

- **SVG icons, never emoji** anywhere user-facing (site + manifest). See `ICONS.md`.
- **`docs/ids.json` must mirror the root `ids.json`** — the site fetches the `/docs` copy. When you
  add a grammar + its UUID to the root `ids.json`, copy it into `docs/ids.json` too (`cp ids.json docs/`).
- **Repo is canonical** — edit grammars here; the app syncs from the repo. Keep the 1:1
  emanation pairing between `kali` and `paradevi`.
- **Reflective, never predictive** — the facts are real astronomy; the meaning is the reader's. A
  card is a prompt, not a prophecy.
