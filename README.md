# design-skills

One repo with every web and app design skill I use, vendored in the [Agent Skills](https://agentskills.io) format so Replit Agent, Claude Code, Cursor, Codex and the `npx skills` CLI can all load them from a single GitHub link.

All 50 skills live flat under `skills/<name>/SKILL.md`.

## Use in Replit

1. In Replit Agent chat, open the **+** menu, choose **Use a skill**, then **Import from GitHub**.
2. Paste this repo's URL and select **Preview skills**.
3. Tick the ones you want and select **Import**. Replit copies them into the project's `.agents/skills/` folder.

Replit allows up to 50 skills per import, which is exactly what this repo holds. Import everything in one pass, or just the groups you need.

To import a single skill, paste the folder URL instead, for example `.../tree/main/skills/impeccable`.

## Use anywhere else

```bash
npx skills add rwstephenalexs-design/design-skills
```

Or copy any `skills/<name>` folder into `.claude/skills/`, `.cursor/skills/` or `.agents/skills/`.

## What is inside

| Group | Skills | Upstream |
|---|---|---|
| Frontend design director | `impeccable` | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) · [impeccable.style](https://impeccable.style) |
| Taste, layout, type, scenes | `taste-skill` | [leonxlnx/taste-skill](https://github.com/leonxlnx/taste-skill) |
| Design intelligence (styles, palettes, fonts, UX rules, stacks) | `ui-ux-pro-max`, `design`, `design-system`, `brand`, `banner-design`, `slides`, `ui-styling` | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| Extract a design profile from references | `design-dna` | [zanwei/design-dna](https://github.com/zanwei/design-dna) |
| 84 ready-made DESIGN.md files | `design-md-library` | [voltagent/awesome-design-md](https://github.com/voltagent/awesome-design-md) |
| Graphics and motion orchestration (web, SwiftUI, Compose, R3F) | `genjutsu` | [AThevon/genjutsu](https://github.com/AThevon/genjutsu) |
| GSAP, official | `gsap-core`, `gsap-timeline`, `gsap-scrolltrigger`, `gsap-plugins`, `gsap-utils`, `gsap-react`, `gsap-performance`, `gsap-frameworks` | [greensock/gsap-skills](https://github.com/greensock/gsap-skills) |
| Motion design principles | `motion-design` | [lottiefiles/motion-design-skill](https://github.com/lottiefiles/motion-design-skill) |
| Three.js | `threejs-fundamentals`, `threejs-geometry`, `threejs-materials`, `threejs-textures`, `threejs-lighting`, `threejs-animation`, `threejs-interaction`, `threejs-loaders`, `threejs-asset-pipeline`, `threejs-shaders`, `threejs-postprocessing`, `threejs-performance`, `threejs-react-three-fiber` | [cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills) |
| Emil Kowalski's design engineering | `animate`, `animate-expo`, `animation-performance`, `animation-vocabulary`, `apple-design`, `ask-sonner`, `break-ui`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations`, `write-swift` | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| Browser automation for visual checks | `playwright-cli` | [microsoft/playwright-cli](https://github.com/microsoft/playwright-cli) |

## Notes on specific skills

- **gsap** – the [greensock/gsap](https://github.com/greensock/gsap) repo is the library itself and has no skill files. The official agent skills live in `greensock/gsap-skills`, which is what is vendored here. Install the library in your project with `npm i gsap`.
- **ui-ux-pro-max** – generated with the upstream CLI (`uipro init --ai universal`) so its `search.py` paths point at `.agents/skills/ui-ux-pro-max/`, which is where Replit puts it. Needs Python 3, no extra packages.
- **impeccable** – the launcher in `skills/impeccable/scripts/` downloads a small binary on first run. Works on Linux and macOS shells; on Windows use `impeccable.cmd`.
- **genjutsu** – vendored from the hosted bundle at `genjutsu.athevon.dev`, which packs the router plus `cast`, `paint`, `bunshin` and all `_jutsu` modules into one skill.
- **playwright-cli** – needs the CLI: `npm i -g @playwright/cli@latest`.
- **taste-skill** and **design-dna** – ship Node scripts (`.mjs`) that run with Node 18+.

## Updating

Each skill is a plain copy of its upstream folder at the time of vendoring. To refresh one, re-copy it from the upstream repo listed above. Only `design-md-library/SKILL.md` is written here; everything else is unmodified upstream content.

## Licenses

Every upstream license is reproduced in [`LICENSES/`](LICENSES/). All sources are MIT except impeccable and playwright-cli, which are Apache 2.0. Copyright stays with the original authors.
