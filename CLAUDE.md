# CLAUDE.md — LM Studio Website

## Project Overview

Single-file interior design website for **LM Studio by Lucie Medgenberg**.
Deployed on Vercel. All code lives in `index.html`.

**Live reference site: [lmstudio.design](https://lmstudio.design)**
Use this as the canonical reference for design decisions, content, and tone. New work should match or improve on what is live there.

---

## Design System

### Colour Palette

| Token | Hex | Usage |
|---|---|---|
| Background | `#C5BBB0` | Page background, section fills |
| Text | `#5C4A3B` | Body copy, headings, icons, borders |
| Text (light) | `#5C4A3B` at ~60% opacity | Captions, metadata, secondary labels |

Use only these two colours. No black (`#000`), no pure white (`#fff`), no greys outside this palette. All borders, dividers, and decorative lines must use `#5C4A3B` (with opacity as needed).

### Typography

- **Headings**: Serif font (e.g. `Cormorant Garamond`, `Playfair Display`, or system serif). Set in normal or light weight — never bold for display sizes.
- **Navigation & Labels**: All-caps, tracked (`letter-spacing: 0.15em` or wider). Sans-serif or light serif.
- **Body copy**: Comfortable line height (~1.7). Modest font size (15–17px).
- **No font stacks outside the defined fonts.** If adding a new typeface, document it here.

### Logo Treatment

```
LM        ← bold serif, large
STUDIO    ← light weight, tracked all-caps, smaller
```

These two elements should remain visually separated (size, weight). Never set them at the same size/weight.

### Tone & Voice

- Refined, restrained, architectural
- Tagline register: "Modern, Timeless, or Heritage Inspired"
- Avoid casual language, exclamation marks, or tech startup phrasing
- Descriptions lean poetic and precise — materials, light, proportion

---

## Structure

### Single HTML File

Everything lives in `index.html`. Do not split into multiple files unless Vercel build tooling is introduced (and document that decision here if it happens).

### Sections (in order)

1. **Header / Hero** — logo, nav, tagline
2. **Services** — what LM Studio offers
3. **Galerie** — portfolio / image grid
4. **Contact** — enquiry form or contact details

### Navigation Labels

Navigation uses **French labels**:

| Section | Nav Label |
|---|---|
| Services | SERVICES |
| Gallery | GALERIE |
| Contact | CONTACT |

All nav labels: all-caps, tracked. Do not translate nav labels to English.

---

## Bilingual Content

The site is **English/French bilingual**. Follow these rules:

- **Primary language**: English for body content unless a section is explicitly French
- **Nav**: Always French (see above)
- **Section headings**: Can be French or bilingual (e.g. "GALERIE" not "Gallery")
- **Do not mix languages mid-sentence.** Full French or full English per block.
- When adding new copy, default to English and note where French translation is needed.

---

## Edit Patterns

### Adding a New Section

1. Follow the existing section HTML structure (wrapper > container > content)
2. Use `#C5BBB0` background or transparent (inherits page background)
3. Use `#5C4A3B` for all text and borders
4. Add a nav anchor (`id="section-name"`) and a matching nav link
5. Nav link label must follow French convention (see above)

### Changing Colours

Do not introduce new colours. If a colour change is needed:
- Update the CSS variable or hex value at the top of the `<style>` block
- Change it in exactly one place — never hardcode colours inline

### Updating the Logo

The logo is set in HTML/CSS, not an image file. Edit the two-part treatment directly in the header markup. Preserve the weight/size contrast between "LM" and "STUDIO".

### Adding Images (Galerie)

- Use square or portrait-oriented images for the grid
- All images should feel editorial: interiors, materials, architectural detail
- No stock photography with visible people in casual settings
- Image captions (if any): light, tracked all-caps in `#5C4A3B`

### Forms (Contact)

- Form fields: minimal border (1px `#5C4A3B` at ~40% opacity), no fill or `#C5BBB0` fill
- Submit button: `#5C4A3B` background, `#C5BBB0` text — or outlined variant
- No placeholder text that disappears on focus without a label alternative

---

## Deployment

- Hosted on **Vercel**
- Push to `main` branch triggers deploy
- No build step — static HTML, deployed as-is
- Do not add `package.json`, bundlers, or build tools unless explicitly requested

---

## What NOT to Do

- Do not add animations heavier than a simple fade or opacity transition
- Do not introduce a JavaScript framework (React, Vue, etc.)
- Do not add fonts, colours, or UI patterns that break the warm greige / deep brown palette
- Do not bold body copy or use all-caps for anything other than nav and labels
- Do not add cookie banners, popups, or modals unless requested
