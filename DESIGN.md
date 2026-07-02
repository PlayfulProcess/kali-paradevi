# DESIGN — kali-paradevi

Author: PlayfulProcess. Status: seed, 2026-07-02.

## 1. Two modes, one system

A mode is a **lens, not a fork**. There are not two decks maintained in parallel; there is one system of **paired items**. Each Kali item (a black hole, void, or dark-mass phenomenon) has a Paradevi counterpart (a galaxy or radiant phenomenon), and each pair is joined by an `emanation` cross-reference.

Why "emanation" and why the link is **bidirectional**: in the corpus grounding (`research/wallis-grounding.md`), Wallis's actual framing is that Kālī and Parā are "two sides of the same coin... aspects of each other" — not a one-way hierarchy where one produces the other. Emanation language in the Krama material describes the Goddess's own cycle (the Twelve Kālīs emanating from, and subsumed back into, Mahākālī). So in this system:

- `emanation` is the name of the **link between a pair**, honored from the tradition's vocabulary.
- The link has **no privileged direction**. Flipping Kali-to-Paradevi and Paradevi-to-Kali are the same move seen from opposite sides.
- Casting can make the emanation move interactive: draw a card in your current mode, then flip it to meet its counterpart.

Design consequence: pairings are curated for real resonance (see `research/objects-shortlist.md`), not generated. A pair should survive the "one-line reason" test — e.g. Sgr A* ↔ Milky Way: *the void at the heart of our own radiance.*

## 2. Item shape

Two layers per item, kept strictly separate so the honesty stance is enforceable in data:

### Astronomy layer (facts — verifiable, sourced)

```json
{
  "id": "kali-sgr-a-star",
  "mode": "kali",
  "name": "Sagittarius A*",
  "catalog_id": "Sgr A*",
  "object_type": "supermassive black hole",
  "constellation": "Sagittarius",
  "distance": "~26,000 light-years",
  "fact": "Imaged by the Event Horizon Telescope in 2022; about 4 million solar masses at the center of our galaxy.",
  "image": {
    "src": "<EHT/NASA/ESO URL>",
    "credit": "EHT Collaboration",
    "license": "CC BY 4.0"
  }
}
```

### Reflective layer (meaning — explicitly interpretive)

```json
{
  "theme": "the still point that everything orbits",
  "prompt": "What in your life is invisible but organizes everything around it?",
  "shadow_reading": "What you refuse to look at does not stop exerting gravity.",
  "light_reading": "A center can hold without being seen.",
  "emanation": "paradevi-milky-way",
  "emanation_reason": "the void at the heart of our own radiance"
}
```

In grammar JSON these merge into one item with clearly named sections (e.g. `The Object` for facts, `The Mirror` for reflection), so a reader always knows which register they are in. Keywords come from both layers.

## 3. Casting shapes (design later, name now)

- **Draw one, flip it** — the core move. Draw in your mode; sit with the card; flip along the `emanation` link and meet the counterpart. The reading is the *pair*, not the card.
- **The wheel of the galactic neighborhood** — a spatial spread: nearby objects (Local Group, Local Void, Great Attractor) arranged as an actual map of where we live; positions mean something because they are real.
- **Deck x mode** — the same spread cast in Kali or Paradevi register produces different content from the same underlying pairs (mirrors the tarot spread-oracle idea: spread = a grammar).

## 4. Visual language

- **Kali (dark mode):** EHT ring-shadow imagery, gravitational-wave visualizations, void maps, X-ray composites. Black field, single sources of light.
- **Paradevi (light mode):** Hubble / JWST / ESO full-radiance imagery — spiral arms, star nurseries, cluster fields. Light field, structure everywhere.

### Image sources and licenses (verify per image before shipping)

| Source | Typical license | Note |
|---|---|---|
| NASA (incl. Chandra, Hubble via STScI) | Public domain (US government work) | Follow NASA media guidelines; some items include third-party material |
| ESA/Hubble | CC BY 4.0 | Credit line required |
| ESA/Webb | CC BY 4.0 | Credit line required |
| ESO | CC BY 4.0 | Credit line required |
| EHT (M87*, Sgr A* images) | CC BY 4.0 | Credit "EHT Collaboration" |
| NSF/LIGO | Generally free with credit | Verify per asset |

Every item's `image` object carries `credit` and `license` inline — same pattern as the commons_image_search pipeline already in recursive.eco MCP.

## 5. Theming note (platform reality)

Today, an app grammar **cannot force the UI into dark or light mode** — recursive.eco has no per-grammar theming hook. So for v1:

- Mode is expressed as **content + imagery first**: a Kali item is dark because its image, register, and readings are dark, regardless of the user's UI theme.
- If a platform theming feature arrives later, mode should be **inferred from the data** (e.g. from `mode` fields on items being viewed), never stored as a grammar-level "type" — keeps grammars portable and the schema honest.

## 6. Values (inherited, enforced in design)

- **Meaning-making over fortune-telling** — the tarot's game-to-mirror framing; the reflective layer asks, never tells.
- **Non-consent axiom** — no card text may claim authority over the user ("you are...", "you will..."). Prompts are questions; readings are offered framings.
- **Honesty about what it is** — facts and mirror kept in separate, labeled layers; no astronomy claim without a verifiable basis.
- **Grief and play coexist** — the Kali mode is allowed to be genuinely about endings, dissolution, and time; the system does not sanitize the dark to stay palatable, and does not solemnize the light to stay serious.

## Charts without doctrine — the adaptive sky (builder, Jul 2 2026)

Not inherited zodiacal doctrine. **No signs, no houses, no birth-chart claims.** Objects are
selected for what they actually are, not for where they sit relative to Earth's ecliptic.

What replaces the chart: **times and places in the sky, connected — as invitation, not claim.**
The system never asserts that the moment you were born was deterministic. But if YOU want to hold
that moment as meaningful — special enough to have left a mark worth contemplating — you can
investigate it as a chart. The belief is the user's to bring; the system supplies an honest sky.
(This is the non-consent axiom applied to astrology.)

**The caster casts MAPS, not cards.** Copy the tarot spread machinery (the platform's
channel-defined casting shapes): where tarot's shape is a spread of card positions,
kali-paradevi's shape is a cast SKY MAP — a time + place resolved into what was actually
overhead, rendered in the dual-mode visual language, each object flippable through its
emanation pair.

**"How to read your chart" is an artwork, not a manual.** Contemplation surfaces use the
recursive.eco spiral-animation language — backgrounds of spirals that keep appearing while
someone sits with a reading — instead of doctrinal how-to text.

**Reading lenses are OURS — never attributed to thinkers who didn't say them.** A lens like
"read the card as a mirror of what is not yet lived" is our creation, influenced by depth
psychology, and is presented as ours (no "— Jung" on words Jung never said). Lenses are the
adaptive ways a person relates to a reading, and lens visibility is a CHANNEL CUSTOMIZATION:
each channel (and possibly each page) chooses whether lenses render, which ones, or none.
(Note: recursive-tarot currently has lens texts attributed to named thinkers in
viewers/voices.json + course MDX — flagged for the same fix.)
