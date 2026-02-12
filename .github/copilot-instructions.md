## Purpose
This repository contains the José Rizal Virtual Experience Gent project (see [README.md](README.md)). These instructions help AI coding agents be immediately productive by describing the project's structure, priorities, and discoverable conventions.

## Big picture
- **What:** A web-based virtual tour + interactive storytelling + an educational mini-game focused on José Rizal and related heritage sites in Ghent.
- **Major components (expected):** front-end web tour (360° images, hotspots), multimedia assets (audio, video, images), an educational game module, and visual/design assets managed in collaboration with partner students.
- **Why structure matters:** multimedia assets are large and separate from code; keep assets in dedicated folders and reference them from the web app to avoid bloating source files.

## Key files & locations
- **Project overview:** [README.md](README.md)
- Visual/illustrative materials: `introductieposter/` and `Project Canvas/` at repo root. Use these as canonical design references.

## Developer workflows (discoverable)
- This repo currently has no build config (no `package.json`, `pyproject.toml`, or similar). When you add code, include a minimal build/dev script and list it in `README.md`.
- Recommended dev commands to add to `README.md` when implementing a web front-end:

  - Install: `npm install` (add `package.json`)
  - Dev server: `npm run dev` or `npm start`
  - Build: `npm run build`

Only document real commands after you add them — do not assume toolchains until they exist in the repo.

## Project-specific conventions and patterns
- Keep multimedia assets separated from code. Create top-level folders like `assets/360`, `assets/audio`, `assets/video`.
- Use descriptive filenames that include location and content, e.g. `gent_stadhuis_360.jpg`, `rizal_house_audio_nl.mp3`.
- When adding interactive hotspots, store metadata as JSON alongside assets (example schema: `assets/360/gent_stadhuis.json` with fields `title`, `coords`, `media`, `transcript`).

## Integration points & external dependencies
- Expect integration with multimedia hosting (CDN or object storage) for large files — do not commit large binaries directly to the repo.
- Collaborations: assets and visual designs come from partner students; track those inputs in the `introductieposter/` and `Project Canvas/` folders.

## How AI agents should behave here
- Prefer small, incremental changes: add a `package.json` and a simple `index.html` when introducing a front-end.
- When adding code, include a short `README.md` update describing how to run the new component.
- Do not add or modify large binary assets without explicit instruction from maintainers.
- If you propose architectural changes (e.g., add a backend), state required infra and provide a minimal runnable example.

## Examples from this repo
- Use [README.md](README.md) as the authoritative project overview and product goals.
- Refer to `introductieposter/` and `Project Canvas/` for visual and content expectations when proposing UI or narrative changes.

## If something is missing
- If builds/tests are absent, create minimal reproducible scaffolding and update `README.md` with commands.
- Ask maintainers for preferred hosting and asset storage before uploading large files.

Please review these instructions and tell me which sections need more detail or examples from other files.
