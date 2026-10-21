---
name: design-md-library
description: Library of 84 ready-made DESIGN.md files extracted from real websites (Linear, Apple, Notion, Figma, Raycast, Vercel, Stripe-style SaaS, car brands, fintech, dev tools and more). Use when the user wants a page or app to look like a specific brand or site, asks for a DESIGN.md starting point, or wants a reference design language (colors, type, spacing, components, motion) to build against.
---

# DESIGN.md library

A DESIGN.md is a plain-markdown design system an agent reads before building UI: palette, typography, spacing, radii, shadows, component rules, motion and voice. This skill ships 84 of them under `design-md/`, one folder per site, extracted by VoltAgent's awesome-design-md project.

## How to use

1. List the available sites: `ls design-md/` (relative to this skill folder). Folder names are the site or brand, e.g. `linear.app`, `apple`, `notion`, `raycast`, `figma`, `posthog`, `mercury`, `oura`.
2. Pick the closest match to what the user asked for. If they named a brand, use that folder. If they described a feel ("clean dev-tool SaaS", "luxury automotive", "playful consumer app"), open two or three candidates and choose the one whose tokens fit.
3. Read `design-md/<site>/DESIGN.md` in full before writing any UI.
4. Copy it into the user's project root as `DESIGN.md` (or merge the relevant sections into an existing one). Tell the user which source you used.
5. Build against it: use its tokens verbatim, keep its spacing scale and type ramp, and follow its component and motion rules. When a token is missing, derive it from the nearest one rather than inventing a new value.

## Pairing with other skills

- `impeccable` and `taste-skill` consume a project DESIGN.md directly. Drop the chosen file in first, then run those skills.
- `ui-ux-pro-max` can generate a fresh design system when no reference site fits.
- `design-dna` extracts a profile from screenshots when the user has a reference that is not in this library.

## Rules

- These files describe a site's visual language, not its trademarks. Use them as a design-system starting point, never to clone a brand's identity, logo, or copy.
- Do not claim the result is affiliated with the source site.
