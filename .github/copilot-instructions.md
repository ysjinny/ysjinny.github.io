# Copilot / AI Agent Instructions for this repo

Purpose: Help AI coding agents be immediately productive editing and extending this site.

Big picture
- This repository is a small Jekyll-based personal site (GitHub Pages). Key files:
  - [/_config.yml](_config.yml) shows `theme: minima` and site metadata.
  - [/index.html](index.html) is the homepage (Jekyll front-matter + layout `default`).
  - [/notes.md](notes.md) is the primary content/notes page.
  - [/assets/css/style.css](assets/css/style.css) contains all styling and CSS variables.

What to change and how
- Content: update or add markdown files (front-matter required for pages/posts). Keep Jekyll front-matter (the YAML block at file top).
- Styling: edit [/assets/css/style.css](assets/css/style.css). The project uses CSS variables in `:root` and BEM-like class names (e.g. `.hero`, `.hero__card`).
- Layout: site uses the `minima` theme declared in `_config.yml`; avoid changing theme without updating `_config.yml`.

Local developer workflow (reproducible commands)
- If you have Ruby + Jekyll installed, preview locally:

```bash
# preferred (with bundler if project has a Gemfile)
bundle exec jekyll serve

# or, if you use a system jekyll install
jekyll serve
```

- Build static site into `_site` for inspection:

```bash
jekyll build
```

Project-specific conventions
- Pages include Jekyll front-matter. Do not remove the leading `---` block in files like [/index.html](index.html).
- Paths to assets use root-based URLs (e.g. `/assets/css/style.css`). When editing CSS, prefer modifying variables in `:root` for theme-wide changes.
- There are no automated tests or CI defined in this repo; changes are primarily content+styling.

Integration points and cautions
- This repo is intended for GitHub Pages; pushes to `main` (or configured branch) will publish the site. Avoid committing generated `_site` directory.
- Notes mention external agent/harness experiments (personal tooling). Those harnesses are NOT present here — do not assume runtime code for agents exists in this repo.

Examples (common edits)
- To add a new note page, create `my-note.md` with front-matter:

```md
---
layout: default
title: My Note
---

Content here.
```

- To change the hero headline, edit [/index.html](index.html) (the H1 inside `.hero`).

When unsure
- Prefer minimal, content-focused pull requests. Describe visual or content changes and include a screenshot of the rendered `_site` when relevant.
- If a change touches build/runtime tooling (adding a Gemfile, changing theme), ask the repo owner before making the change.

If anything here is unclear or you'd like more detail (e.g., typical branch names, CI, or publishing flow), tell me which part to expand.
