<p align="center">
  <strong>English</strong> · <a href="README_zh.md">中文</a>
</p>

<h1 align="center">BIUE 🐾 · Codex Pet</h1>

<p align="center">
  <strong>A tiny code supervisor with very large ears</strong><br>
  Runs when Codex is busy, waves when noticed, and accepts payment in attention.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Pet%20v2-111827?style=flat-square" alt="Codex Pet v2">
  <img src="https://img.shields.io/badge/Atlas-1536%C3%972288-2F8F83?style=flat-square" alt="1536 by 2288 atlas">
  <img src="https://img.shields.io/badge/Animations-9%20states-E76F51?style=flat-square" alt="9 animation states">
  <img src="https://img.shields.io/badge/Look-16%20directions-F4A261?style=flat-square" alt="16 look directions">
  <img src="https://img.shields.io/badge/License-MIT-7C3AED?style=flat-square" alt="MIT License">
</p>

<p align="center">
  <a href="#overview">Meet BIUE</a> ·
  <a href="#showcase">Cat in action</a> ·
  <a href="#specification">Nerdy bits</a> ·
  <a href="#installation">Bring him home</a> ·
  <a href="#repository-map">What's in the box</a> ·
  <a href="#license">MIT</a>
</p>

<a id="overview"></a>
## Meet BIUE 🐈

BIUE (小布鲁) is based on my own blue Abyssinian. He has huge ears, amber eyes, a turquoise-and-gold collar, and the quiet confidence of someone who has never fixed a bug in his life.

Yes, **BIUE** with an I. That is his name, not your spell-check having a difficult day.

His job description is simple:

- run around while Codex works;
- wave a paw when the moment calls for it;
- look personally devastated when something fails;
- inspect your cursor from 16 different directions;
- provide moral support while taking no responsibility whatsoever.

The animation uses the original painted frames only. No stretchy-cat interpolation, no squashed whiskers, no accidental noodle legs.

<a id="showcase"></a>
## Cat in action 🎬

### The whole cat drawer

<p align="center">
  <img src="previews/contact-sheet.png?v=d2552a6" width="900" alt="Contact sheet showing the refined BIUE Codex pet animations">
</p>

### A very busy employee

| Idle | Waving | Working | Waiting |
| --- | --- | --- | --- |
| ![BIUE idle animation](previews/idle.gif?v=d2552a6) | ![BIUE waving animation](previews/waving.gif?v=d2552a6) | ![BIUE working animation](previews/running.gif?v=d2552a6) | ![BIUE waiting animation](previews/waiting.gif?v=d2552a6) |

### Mouse-pointer surveillance

<p align="center">
  <img src="previews/look-directions.png?v=d2552a6" width="900" alt="Neutral pose and sixteen clockwise look directions">
</p>

He can also sprint left, sprint right, jump, sulk after failure, and perform a highly qualified code review. The evidence is in [`previews`](previews/).

<a id="specification"></a>
## Nerdy bits 🔧

| Property | Value |
| --- | --- |
| Sprite contract | Codex Pet v2 |
| Atlas file | `spritesheet.webp` |
| Atlas dimensions | 1536 × 2288 px |
| Grid | 8 columns × 11 rows |
| Cell dimensions | 192 × 208 px |
| Standard states | 9 |
| Action pacing | Lossless adjacent-frame smooth loops |
| Look directions | 16, clockwise in 22.5° steps |
| Transparency | RGBA WebP |
| Manifest | `pet.json` with `spriteVersionNumber: 2` |
| Validation | Passed with 0 errors and 0 warnings |

One tiny cat-flap problem: this repo works with Codex desktop/CLI v2 only. ChatGPT's web pet picker uses a different 1536 × 1872 layout and needs a converted sprite sheet; this particular `spritesheet.webp` will not squeeze through that door unchanged.

<a id="installation"></a>
## Bring him home 🏠

### 1. Pick up the cat carrier

```bash
git clone https://github.com/rudykon/codex-pet-blue.git
cd codex-pet-blue
```

### 2. Give BIUE a room

#### Windows PowerShell

```powershell
$petDir = "$env:USERPROFILE\.codex\pets\xiaobulu"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\pet.json, .\spritesheet.webp -Destination $petDir
```

#### macOS / Linux

```bash
mkdir -p ~/.codex/pets/xiaobulu
cp pet.json spritesheet.webp ~/.codex/pets/xiaobulu/
```

### 3. Open the door

The folder stays named `xiaobulu`, while the visible name **小布鲁** comes from `pet.json`. Refresh or restart Codex and he should appear automatically in the pet selector. In the Codex CLI, `/pets` opens the local cat census.

<a id="repository-map"></a>
## What's in the box 📦

| Path | Purpose |
| --- | --- |
| [`pet.json`](pet.json) | Pet identity, display name, description, sprite version, and atlas path |
| [`spritesheet.webp`](spritesheet.webp) | Complete transparent v2 animation atlas |
| [`previews/contact-sheet.png`](previews/contact-sheet.png) | Visual overview of all animation rows |
| [`previews/look-directions.png`](previews/look-directions.png) | Neutral pose and the 16-direction attention loop |
| [`previews/`](previews/) | Per-state animated GIF previews |
| [`validation.json`](validation.json) | Machine-readable atlas validation result |
| [`LICENSE`](LICENSE) | MIT License terms covering the repository |

<a id="license"></a>
## MIT, because cats hate paperwork 📜

BIUE's artwork, animations, previews, metadata, and docs are released under the [MIT License](LICENSE). Take him home, remix him, teach him new tricks, or put him in your own project, including commercial ones. Just keep the copyright and license notice with the copies.

Codex, ChatGPT, and OpenAI are OpenAI trademarks. BIUE is a community cat, not an OpenAI employee. Please do not ask him about your API bill.
