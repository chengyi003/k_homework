<!-- .github/copilot-instructions.md for k_homework -->
# Quick instructions for AI coding agents

This repository is a small static HTML homework collection. The guidance below helps an AI agent be immediately productive when editing, refactoring, or adding content.

- Project type: static HTML site — no build system, frameworks, or package manager detected.
- Primary content: dated folders named `sYYYYMMDD/` containing HTML files and an `images/` subfolder with media.

Key patterns and conventions
- Each `sYYYYMMDD/` folder groups a day's homework. Edit or add files in the appropriate folder.
- HTML files are plain static pages. Prefer minimal, non-invasive edits: preserve relative paths to `images/` and other local files.
- Image references are relative (e.g. `images/p01.jpg` in `s20251007/`). Keep filenames and casing exact (Windows is case-insensitive, but other environments may not be).

Files to inspect for context
- `README.md` — repository root (small/empty). Use it only for very high-level context.
- Examples: `s20251015/s20251016/link.html`, `s20251015/nav.html`, `s20251007/song.html` — look at these when changing layout or link patterns.

Developer workflows
- No build/test commands required — repository contains static files. To preview changes, open the HTML file in a browser or use a simple static server (e.g., `python -m http.server 8000` in the workspace root).

Editing guidance (concrete rules)
- When adding new assets, place them in the relevant `images/` subfolder next to the HTML that references them.
- Preserve existing indentation and HTML formatting style used in nearby files.
- If creating new dated folders, follow the `sYYYYMMDD` naming convention.

Examples (how to perform common edits)
- To add a new page for 2025-10-20: create `s20251020/s20251020_01_topic.html` and an `images/` folder if needed.
- To fix a broken image in `s20251007/song.html`: confirm the file exists at `s20251007/images/p01.jpg` and that the `<img>` src uses the relative path `images/p01.jpg`.

What not to do
- Do not introduce tooling (npm, webpack, etc.) without explicit request from the repository owner.
- Avoid large automated refactors across many dated folders; prefer small, targeted edits and ask before bulk changes.

When to ask the user
- If a change touches more than one dated folder or modifies many files, ask for clarification on desired global behavior.
- Ask when proposing to add a build system or to convert these static pages into a site generator (e.g., Jekyll/Next) — that's a larger migration.

Contact / verification
- After making edits, recommend the user preview changed pages in a browser and confirm visual correctness.
