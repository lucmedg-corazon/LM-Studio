# PROJECT.md — LM Studio

## What This Is

Personal website for **LM Studio**, an interior design practice by **Lucie Medgenberg**.

The site presents the studio's work, services, and contact details. It is intentionally minimal — one HTML file, no framework, no CMS.

**Live site:** [lmstudio.design](https://lmstudio.design) — the canonical reference for design, content, and tone. New work should match or improve on what is live there.

---

## Goals

- Present LM Studio as a refined, credible interior design practice
- Attract clients seeking modern, timeless, or heritage-inspired interiors
- Provide a clear way for prospective clients to make contact
- Load fast, look beautiful, require zero maintenance overhead

---

## Audience

Prospective clients commissioning residential or commercial interior design — likely design-literate, French or English speaking, attracted to architectural restraint and quality materials.

---

## Tech Stack

| Layer | Choice |
|---|---|
| Code | Single `index.html` (HTML + CSS + minimal JS) |
| Hosting | Vercel (static) |
| Fonts | Google Fonts or system serif stack |
| Images | Static assets committed to repo or linked externally |
| Build | None — file deploys as-is |

---

## Brand

| Attribute | Value |
|---|---|
| Studio name | LM Studio |
| Founded by | Lucie Medgenberg |
| Tagline | Modern, Timeless, or Heritage Inspired |
| Background | `#C5BBB0` (warm greige) |
| Text | `#5C4A3B` (deep warm brown) |
| Logo | "LM" bold serif + "STUDIO" light tracked caps |
| Languages | English (primary) + French (nav labels, select headings) |

---

## Site Sections

### Header
Logo + navigation. Navigation links: SERVICES · GALERIE · CONTACT (French labels, tracked all-caps).

### Services
Description of what LM Studio offers — scope of work, project types, approach.

### Galerie
Portfolio imagery. Grid of interior photography or project documentation.

### Contact
Enquiry form or contact details for prospective clients.

---

## Current Status

- [ ] `index.html` created with full section structure
- [ ] Design system implemented (palette, typography, logo)
- [ ] Services copy written
- [ ] Galerie images selected and placed
- [ ] Contact form wired up
- [ ] Deployed to Vercel

---

## Key Decisions

**Single HTML file** — chosen for zero-maintenance simplicity. No build tools, no dependencies, nothing to break. Revisit only if content management or a blog is introduced.

**French nav labels** — reflects the bilingual identity of the studio and adds refinement. Body content remains English unless specifically written in French.

**No JavaScript framework** — the site does not need reactivity. Vanilla JS only, and only if needed for the contact form.
