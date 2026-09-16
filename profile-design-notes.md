# Neo-Brutalist Profile Design Notes & Decision Log

This document details the architectural choices, custom SVG asset design, accuracy controls, visual design rationale, link verification results, and GitHub rendering constraints applied during the redesign of the GitHub Profile README for **Bharanidharan S** ([`bharanx`](https://github.com/bharanx)).

---

## 1. Design System & Visual Identity Concept

The profile has been completely redesigned using a **Neo-Brutalist + Editorial Design System with Custom SVG Animations**:
* **Visual Language**: Heavy typography, high contrast, hard rectangular blocks, thick 3-4px solid black borders, sharp corners, hard-edge drop shadows (`#CCFF00`), monospace metadata labels, and numbered section headers (`01 / ABOUT`, `02 / SELECTED WORK`, `03 / TOOLBOX`, `04 / CURRENTLY`, `05 / ACTIVITY`, `06 / INTERNET`).
* **Color Palette**:
  - Primary Base: Dark Charcoal `#0F0F12` & Off-White `#FAFAFA`
  - Accent: Acid Yellow / Electric Yellow `#CCFF00`
  - Borders & Shadows: Pure Black `#000000`
* **Typography Hierarchy**: Stencil Impact headers (`Impact`, `Arial Black`), Monospace metadata (`Fira Code`, `Consolas`), and clean body text.

---

## 2. Custom Visual Asset Inventory (`assets/`)

| Asset File | Visual Description | Animation / Feature |
| :--- | :--- | :--- |
| [`assets/hero.svg`](file:///d:/Git%20Profile/assets/hero.svg) | Neo-brutalist header card with window controls, `BHARANIDHARAN S` stencil title, live status badge, and tagline box. | Blinking prompt cursor `_`, pulsing live status dot, and 360° rotating brutalist star. |
| [`assets/marquee.svg`](file:///d:/Git%20Profile/assets/marquee.svg) | Acid-yellow horizontal marquee divider banner (`BUILD ➔ BREAK ➔ LEARN ➔ REPEAT ➔ SECURE ➔ RESEARCH ➔`). | Infinite horizontal CSS keyframe scroll animation. |
| [`assets/section-01.svg`](file:///d:/Git%20Profile/assets/section-01.svg) | Neo-brutalist numbered section header: `01 / ABOUT ME` with `[ VERIFIED ]` badge. | SVG graphic header block. |
| [`assets/section-02.svg`](file:///d:/Git%20Profile/assets/section-02.svg) | Neo-brutalist numbered section header: `02 / SELECTED WORK` with `[ FEATURED REPOS ]` badge. | SVG graphic header block. |
| [`assets/section-03.svg`](file:///d:/Git%20Profile/assets/section-03.svg) | Neo-brutalist numbered section header: `03 / TECH TOOLBOX` with `[ STACK & TOOLS ]` badge. | SVG graphic header block. |
| [`assets/section-04.svg`](file:///d:/Git%20Profile/assets/section-04.svg) | Neo-brutalist numbered section header: `04 / CURRENTLY` with `[ FOCUS & LABS ]` badge. | SVG graphic header block. |
| [`assets/section-05.svg`](file:///d:/Git%20Profile/assets/section-05.svg) | Neo-brutalist numbered section header: `05 / GITHUB ACTIVITY` with `[ METRICS ]` badge. | SVG graphic header block. |
| [`assets/section-06.svg`](file:///d:/Git%20Profile/assets/section-06.svg) | Neo-brutalist numbered section header: `06 / AROUND THE INTERNET` with `[ LINKS ↗ ]` badge. | SVG graphic header block. |
| [`assets/footer.svg`](file:///d:/Git%20Profile/assets/footer.svg) | Neo-brutalist closing footer card: `KEEP BUILDING. SEE YOU AROUND ↗`. | SVG graphic footer block. |
| [`assets/stickers/sticker-wip.svg`](file:///d:/Git%20Profile/assets/stickers/sticker-wip.svg) | Brutalist yellow tape sticker: `[ WORK IN PROGRESS ]`. | Static SVG graphic sticker. |
| [`assets/stickers/sticker-star.svg`](file:///d:/Git%20Profile/assets/stickers/sticker-star.svg) | 8-point acid yellow brutalist star badge. | Static SVG graphic sticker. |
| [`assets/stickers/sticker-human.svg`](file:///d:/Git%20Profile/assets/stickers/sticker-human.svg) | Brutalist badge: `[ 100% HUMAN CODE ]`. | Static SVG graphic sticker. |
| [`assets/stickers/sticker-ctrlz.svg`](file:///d:/Git%20Profile/assets/stickers/sticker-ctrlz.svg) | Brutalist shortcut box: `[ CTRL + Z ]`. | Static SVG graphic sticker. |

---

## 3. Strict Accuracy Controls & Status Mapping

* **Source of Truth**: All details derived exclusively from [https://portfolio-lake-seven-97.vercel.app/](https://portfolio-lake-seven-97.vercel.app/).
* **ChainProof**: Preserved as a *Research Direction / Major Project started August 2026* (in development; no code or results published yet).
* **NETRA**: Identified as a *College Project Prototype*. Verified repo link (`https://github.com/maajed/defrox-ruf`) is linked.
* **Proof of Work**: Labeled as a *24-Hour Hackathon Prototype* by Team "Peanut Butter". Distinguished implemented tech from *designed concepts* (decentralized identity & blockchain structure) and *planned features* (IPFS). Verified repo link (`https://github.com/bharanx/Proof-Of-Work`) included.
* **PortSwigger Academy**: Labeled as *Upcoming / In Progress Learning*.
* **Excluded Fluff**: Unverified tech (e.g. AWS, GCP, Azure, Kubernetes, Metasploit, Splunk, Terraform) excluded.

---

## 4. Link Verification Log

| Target | URL | Status | Implementation |
| :--- | :--- | :--- | :--- |
| **GitHub Profile** | `https://github.com/bharanx` | Verified Public | Linked in Section 06 |
| **LinkedIn** | `https://linkedin.com/in/bharanidharan-s-4458b5326` | Verified Public | Linked in Section 06 |
| **Live Portfolio** | `https://portfolio-lake-seven-97.vercel.app/` | Verified Live | Linked in Section 06 |
| **Email** | `mailto:bharanibd2007@gmail.com` | Verified Public | Linked in Section 06 |
| **CyLab Handle** | `https://learn.cylabacademy.org/users/bharanx` | Verified Public | Linked in Section 04 |
| **NETRA Repo** | `https://github.com/maajed/defrox-ruf` | Verified Live Repo | Linked in Section 02 |
| **Proof of Work Repo**| `https://github.com/bharanx/Proof-Of-Work` | Verified Live Repo | Linked in Section 02 |

---

## 5. GitHub Rendering Compatibility

* **Image Embedding**: All custom SVGs are embedded via `<img src="assets/..." />` which renders native SVG CSS animations in GitHub Markdown.
* **Responsive Layout**: Designed within standard 800px containers to prevent horizontal scrolling across desktop and mobile screens.
* **Zero JavaScript / Custom CSS Dependencies**: Relies solely on GitHub-supported HTML markup, Markdown code blocks, and standalone SVG files.
