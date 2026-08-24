<p align="center">
  <strong>English</strong> · <a href="README_zh.md">中文</a>
</p>

<h1 align="center">BIUE · Codex Pet</h1>

<p align="center">
  <strong>A curious Abyssinian companion for Codex</strong><br>
  Warm brown fur, bright eyes, a beaded collar, and a complete v2 animation set.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Pet%20v2-111827?style=flat-square" alt="Codex Pet v2">
  <img src="https://img.shields.io/badge/Atlas-1536%C3%972288-2F8F83?style=flat-square" alt="1536 by 2288 atlas">
  <img src="https://img.shields.io/badge/Animations-9%20states-E76F51?style=flat-square" alt="9 animation states">
  <img src="https://img.shields.io/badge/Look-16%20directions-F4A261?style=flat-square" alt="16 look directions">
  <img src="https://img.shields.io/badge/Artwork-All%20rights%20reserved-7C3AED?style=flat-square" alt="Artwork all rights reserved">
</p>

<p align="center">
  <a href="#overview">Overview</a> ·
  <a href="#showcase">Showcase</a> ·
  <a href="#specification">Specification</a> ·
  <a href="#installation">Installation</a> ·
  <a href="#repository-map">Repository</a> ·
  <a href="#usage-and-rights">Usage & Rights</a>
</p>

<a id="overview"></a>
## Overview

BIUE (小布鲁) is a blue Abyssinian cat whose dilute blue coat reads as a distinctive warm brown-gray. BIUE has large upright ears, amber eyes, a turquoise-and-gold beaded collar, and a round name tag. The pet is packaged for the Codex v2 sprite contract and includes all standard activity states plus a continuous 16-direction look loop.

| Goal | Implementation | Result |
| --- | --- | --- |
| Preserve character identity | Stable face, coat, proportions, collar, and name tag across every state | BIUE remains recognizable throughout the atlas |
| Communicate Codex activity | Separate idle, movement, greeting, jumping, failure, waiting, working, and review loops | The pet reacts naturally to task state changes |
| Support pointer-aware attention | Sixteen clockwise look poses in 22.5° steps | Smooth directional attention around the pet |
| Ship a clean package | Transparent WebP, v2 manifest, previews, and deterministic validation | A small, auditable repository ready for local installation |

<a id="showcase"></a>
## Showcase

### Complete animation atlas

<p align="center">
  <img src="previews/contact-sheet.png" width="900" alt="Contact sheet showing all BIUE Codex pet animations">
</p>

### Activity states

| Idle | Waving | Working | Waiting |
| --- | --- | --- | --- |
| ![BIUE idle animation](previews/idle.gif) | ![BIUE waving animation](previews/waving.gif) | ![BIUE working animation](previews/running.gif) | ![BIUE waiting animation](previews/waiting.gif) |

### Look directions

<p align="center">
  <img src="previews/look-directions.png" width="900" alt="Neutral pose and sixteen clockwise look directions">
</p>

The [`previews`](previews/) directory also includes left/right movement, jumping, failure, and review loops.

<a id="specification"></a>
## Specification

| Property | Value |
| --- | --- |
| Sprite contract | Codex Pet v2 |
| Atlas file | `spritesheet.webp` |
| Atlas dimensions | 1536 × 2288 px |
| Grid | 8 columns × 11 rows |
| Cell dimensions | 192 × 208 px |
| Standard states | 9 |
| Look directions | 16, clockwise in 22.5° steps |
| Transparency | RGBA WebP |
| Manifest | `pet.json` with `spriteVersionNumber: 2` |
| Validation | Passed with 0 errors and 0 warnings |

> [!NOTE]
> This is a desktop/CLI v2 package. ChatGPT web custom-pet upload uses a different 1536 × 1872 asset contract, so `spritesheet.webp` should not be uploaded to the web picker unchanged.

<a id="installation"></a>
## Installation

### 1. Clone the repository

```bash
git clone https://github.com/rudykon/codex-pet-blue.git
cd codex-pet-blue
```

### 2. Install the pet

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

### 3. Select BIUE

Refresh or restart Codex, then choose **小布鲁** in the pet selector. In Codex CLI, use `/pets` to view and switch locally installed pets.

<a id="repository-map"></a>
## Repository map

| Path | Purpose |
| --- | --- |
| [`pet.json`](pet.json) | Pet identity, display name, description, sprite version, and atlas path |
| [`spritesheet.webp`](spritesheet.webp) | Complete transparent v2 animation atlas |
| [`previews/contact-sheet.png`](previews/contact-sheet.png) | Visual overview of all animation rows |
| [`previews/look-directions.png`](previews/look-directions.png) | Neutral pose and the 16-direction attention loop |
| [`previews/`](previews/) | Per-state animated GIF previews |
| [`validation.json`](validation.json) | Machine-readable atlas validation result |

## Privacy and responsible sharing

- No original pet photos, EXIF metadata, private identity references, or personal files are included.
- The package contains only approved release artwork, previews, metadata, and validation output.
- Third-party mirrors should preserve the character credit and must not imply official endorsement by OpenAI.
- Compatibility may change as Codex pet specifications evolve; current platform behavior takes precedence over this README.

<a id="usage-and-rights"></a>
## Usage and rights

The repository is shared for personal Codex installation and non-commercial demonstration. BIUE's character design and artwork are **all rights reserved**. Without explicit permission from the creator, do not sell, sublicense, redistribute as a competing pet pack, use as training data, or present the artwork as your own.

Codex, ChatGPT, and OpenAI are trademarks of OpenAI. This community pet is not an official OpenAI product or endorsement.
