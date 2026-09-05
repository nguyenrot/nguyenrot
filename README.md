# Nguyên

Software Engineer · Đà Nẵng

I build backend systems, developer tools, and things I want to exist.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/identity-dark.svg?v=2">
    <img src="./assets/identity-light.svg?v=2" alt="Warm stacked plates with K and N cut through, one inner plate in copper" width="100%">
  </picture>
</p>

## Selected work

### GõViệt

Vietnamese input for macOS. A Unikey-style menu-bar app: type in every program without switching input sources.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/goviet-dark.svg?v=2">
  <img src="./assets/goviet-light.svg?v=2" alt="Telex keys v i e e j t composing to việt, with English text staying as text" width="100%">
</picture>

Rust composes Telex and VNI, then restores English so `text` stays `text`, not `tẽt`. Swift injects per app — fast, paced in terminals, select-and-retype in Chromium — and ignores its own `GVIT` events.

<details>
<summary>Architecture</summary>
<p>Pure composition in Rust (tone placement, syllable validation, fourteen TSV corpora) → C ABI with fixed-size buffers, no allocation on the hot path → Swift <code>EventTapManager</code>, <code>TextInjector</code>, and per-bundle app profiles. A watchdog polls tap health. The signing identity is pinned so Accessibility survives rebuilds. English words that are also valid Vietnamese syllables stay in <code>known_limitations.tsv</code> rather than being papered over. Not notarized yet; the DMG is signed with an Apple Development cert.</p>
</details>

[Repository](https://github.com/nguyenrot/goviet) · [Releases](https://github.com/nguyenrot/goviet/releases)

### <img src="./assets/marks/lattice.svg?v=2" alt="" height="32"> Lattice

One content model, two languages. Nuxt reads; Django and PostgreSQL publish — an API boundary so the reading surface can move on its own.

[lattice.kynguyen.cc](https://lattice.kynguyen.cc)

### <img src="./assets/marks/lumi.svg?v=2" alt="" height="32"> Lumi

Answers arrive as a stream. A per-thread SSE buffer renders each part as it lands; incomplete Markdown is a state to handle, not a bug.

[lumi.kynguyen.cc](https://lumi.kynguyen.cc)

### <img src="./assets/marks/citadel.svg?v=2" alt="" height="32"> Citadel

The rules run without a screen. A headless simulation plays stages with bots before the Canvas art is allowed to change.

[citadel.kynguyen.cc](https://citadel.kynguyen.cc)

The rest of the ecosystem lives at [kynguyen.cc](https://kynguyen.cc).

## How I work

Most of what I ship sits where backend correctness meets software people actually use: APIs that don't silently lie, migrations that don't surprise anyone on Friday, boundaries you can point to. I write the dull parts well — the rest gets easier.

---

## Elsewhere

[kynguyen.cc](https://kynguyen.cc) · [nguyen@kynguyen.cc](mailto:nguyen@kynguyen.cc) · [LinkedIn](https://www.linkedin.com/in/nguyen-pham-ky)
