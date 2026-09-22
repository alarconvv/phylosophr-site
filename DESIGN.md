---
name: phyloSophR community site
description: A plain, content-first explainer for a reproducibility-focused PCM research tool and its community-annotation effort.
colors:
  ink: "#2C3E50"
  muted: "#54696A"
  bg: "#ECF0F1"
  panel: "#DEE2E6"
  panel-strong: "#CED4DA"
  success: "#18BC9C"
  success-ink: "#0E6B57"
  success-bg: "#E8F7F3"
  warning: "#F39C12"
  warning-ink: "#8A5A00"
  warning-bg: "#FDF3E3"
typography:
  display:
    fontFamily: "IBM Plex Sans, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "clamp(30px, 4.6vw, 50px)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "IBM Plex Sans, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "clamp(24px, 3vw, 32px)"
    fontWeight: 650
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  body:
    fontFamily: "IBM Plex Sans, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "IBM Plex Mono, ui-monospace, Menlo, monospace"
    fontSize: "13px"
    fontWeight: 500
rounded:
  sm: "4px"
  md: "6px"
  lg: "8px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: "12px 22px"
  button-primary-hover:
    backgroundColor: "#1c2833"
  button-outline:
    backgroundColor: "#ffffff"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: "12px 22px"
  status-tag:
    backgroundColor: "#ffffff"
    textColor: "{colors.muted}"
    rounded: "{rounded.sm}"
    padding: "5px 11px"
  callout-note:
    backgroundColor: "{colors.success-bg}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "20px 22px"
  callout-status:
    backgroundColor: "{colors.warning-bg}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "20px 22px"
---

# Design System: phyloSophR community site

## Overview

**Creative North Star: "The Lab Notebook"**

phyloSophR's public site is the Persuade-mode sibling of an already-built Operate-mode Shiny tool (`../phylosophr-demo/`), and it deliberately inherits that tool's exact visual system rather than inventing a new one — a dissertation project explaining itself to a research community reads as one artifact wearing two hats, not two products. The register is plain, content-first, and academic: closer to an R-package documentation site (pkgdown, rOpenSci) or a university lab-group page than a marketing landing page. A bolder, more illustrative direction (a herbarium/specimen-label visual world) was offered and explicitly declined by the user in favor of this conventional register, confirmed against pkgdown-style sites and lab-group pages as the craft bar.

Confirmed visual rejections: no hero photography or illustration (none exists, none is invented); no gradient text; no pill-shaped badges; no colored accent borders on cards; no partner-organization logos (none are confirmed partners).

**Key Characteristics:**
- Flat, bordered surfaces on a neutral gray page ground — no soft ambient shadows
- A single ink color (navy) carries nearly all text, headings, and primary interactive elements
- Turquoise marks the community-annotation thread specifically; amber marks "not active yet" honesty notices
- IBM Plex Sans for everything except quoted/annotated text, which switches to IBM Plex Mono
- Rectangular, small status tags — never pills

## Colors

A restrained, mostly-neutral palette where color is reserved for status and one accent thread, not decoration.

### Primary
- **Ink Navy** (`#2C3E50`): all headings, body text, primary buttons, links, and focus rings. Carries the large majority of the page's visual weight — this is a one-color system, not a multi-accent one.

### Secondary
- **Signal Turquoise** (`#18BC9C`) with **Deep Turquoise Ink** (`#0E6B57`) for text and **Pale Turquoise** (`#E8F7F3`) for backgrounds: marks the community-annotation narrative specifically — the annotated-entity highlights in the demonstration card, the "From the proposal" quote callouts, the section kicker for that thread.

### Tertiary
- **Amber** (`#F39C12`) with **Deep Amber Ink** (`#8A5A00`) for text and **Pale Amber** (`#FDF3E3`) for backgrounds: reserved exclusively for honesty/status notices — the "planned, not active yet" callout and the hero's status-tag dot. Never used decoratively.

### Neutral
- **Page Gray** (`#ECF0F1`): the body background.
- **Panel Gray** (`#DEE2E6`) / **Panel Gray Strong** (`#CED4DA`): reserved for future inset-panel and text-selection use; the current page is built entirely on white cards over the page-gray ground.
- **Muted Slate** (`#54696A`): secondary text (subheads, captions, footer copy).
- **Hairline** (`rgba(44,62,80,.14)`): all card and section borders.

### Named Rules
**The One-Ink Rule.** Every heading, paragraph, link, and primary button uses the same navy. Color is never used to create hierarchy among body content — only weight, size, and spacing do that. Turquoise and amber exist to mark two specific narrative threads (the annotation task; honesty about project status), not as general-purpose accents.

## Typography

**Display/Body Font:** IBM Plex Sans (with -apple-system, Segoe UI, Roboto fallback)
**Label/Mono Font:** IBM Plex Mono (ui-monospace, Menlo fallback)

**Character:** IBM Plex Sans is a geometric, engineering-oriented grotesk designed for technical products — the same face already carrying the sibling demo tool's UI, so quoting it here is continuity, not a training-data default. IBM Plex Mono appears specifically wherever real proposal text is quoted or annotated, giving those passages a "primary source" register distinct from the page's own voice.

### Hierarchy
- **Display** (400, `clamp(30px, 4.6vw, 50px)`, 1.15 line-height, -0.03em): the hero H1 only. Uses a `<strong>` (700) inline for the one emphasized word.
- **Headline** (650, `clamp(24px, 3vw, 32px)`, 1.2 line-height, -0.02em): section H2s, max 22ch.
- **Title** (650, 19px): H3 subheads within a section, and step/stat card titles.
- **Body** (400, 16px, 1.6 line-height, max 68ch measure): all paragraph copy.
- **Label** (500–700, 12–13px, uppercase, tracked): section kickers, status tags, callout labels, annotation-demo field keys.

## Layout

Single-column content shell, max-width 880px (`.shell`) for reading sections, 1040px (`.shell--wide`, currently unused but reserved) for anything wider. No sidebar, no multi-column grid beyond the responsive card grids (stat cards, mechanism steps, annotation tag grid) which are `repeat(auto-fit, minmax(...))` and collapse to a single column under ~640px. Sections stack vertically, each separated by a hairline top border (except the hero, which has none above it). Spacing rhythm: 52px section padding at rest, tightening to 40px under 640px; 16–24px internal card padding throughout.

## Elevation & Depth

Flat by default. Cards (stat cards, step cards, the annotation-demo panel) carry a single crisp shadow (`0 1px 2px rgba(44,62,80,.09)`) plus a 1px hairline border — reads as "paper on a table," not "floating glass." No hover-lift, no blur, no layered shadow ramps.

### Named Rules
**The Flat-By-Default Rule.** Depth comes from a 1px border plus a barely-there shadow, never from blur radius or offset beyond 2px. If an element needs to look important, give it a colored callout background (turquoise/amber), not more shadow.

## Shapes

Small, consistent radii: 4px for buttons, tags, and small chips; 6px for cards and callouts; 8px reserved for the largest containers (currently unused on this page, carried over from the sibling app for consistency). No pill shapes anywhere — the status tag and chip components are deliberately rectangular with a small radius, breaking from the rounded-pill convention common to badges. Borders are always 1px, always the hairline ink-tint color, except callouts which use a tinted version of their semantic color at ~50% opacity.

## Components

### Buttons
- **Shape:** 4px radius, 12px/22px padding.
- **Primary:** navy background (`#2C3E50`), white text; hover darkens to `#1c2833`.
- **Outline:** white background, navy text and border; hover darkens border to solid navy.

### Status Tag / Chip
- **Style:** white background, 1px hairline border, 4px radius, 12–13px muted-navy text. The hero's status tag adds a small amber dot (`::before`, 7px circle) to mark "in progress" without needing an icon font.
- **Chips** (partner-organization names): same rectangular-but-softer treatment at 30px radius — the one deliberate pill shape on the page, used only for that one list, since it reads as a tag list rather than a status indicator.

### Cards
- **Corner style:** 6px radius.
- **Background:** white, over the page's gray-200 ground.
- **Shadow:** the flat 1px/2px shadow described above.
- **Border:** 1px hairline.
- **Internal padding:** 18–22px.

### Callouts
- **Note** (turquoise): direct quotations from the proposal.
- **Status** (amber): explicit "this is not active yet" honesty notices. These two are the only two callout variants; there is no third neutral/info variant because none was needed.

### Annotation Demonstration (signature component)
A dark navy card (`background: var(--ink)`, white text) that inverts the page's palette to set the annotated-sentence example apart as a distinct artifact, not more body copy. Annotated terms are marked with a solid turquoise highlight (`<mark>`); the extracted entity/value pairs below render as a responsive grid of small translucent-white tag cards, each with an IBM Plex Mono value. This is the page's one moment of real visual departure from the flat white-card system, reserved for the single most important proof point (a real example, not an interface mockup).

## Do's and Don'ts

### Do:
- **Do** keep the entire page on the single navy ink color for text and primary actions; introduce turquoise or amber only for their specific named roles.
- **Do** quote the proposal verbatim inside turquoise callouts, and mark any illustrative (non-verbatim) content clearly as such.
- **Do** keep buttons, tags, and cards on the 4/6/8px radius scale — no larger radii, no pill shapes outside the partner-chip list.
- **Do** use IBM Plex Mono only for quoted/annotated source material, never for ordinary UI labels.

### Don't:
- **Don't** add a hero illustration, photograph, or icon set — none exists and none should be fabricated for this project.
- **Don't** style the "potential partners" list as if they were confirmed sponsors (no logos, no "trusted by" framing).
- **Don't** add a working-looking signup form, waitlist counter, or member count — the contact section stays a plain mailto link until a real mechanism exists.
- **Don't** introduce a third accent color; the two-thread system (turquoise = annotation, amber = honesty/status) is deliberately exhaustive.
