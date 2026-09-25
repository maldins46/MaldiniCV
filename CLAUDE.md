# CLAUDE.md

## What this is

Single-file LaTeX CV. Template: LuxSleek-CV 1.1 (credit in README.md). Not a software project — no tests, no linting, no package manager.

## Structure

- `src/cv-maldini.tex` — all CV content and layout.
- `src/profile.png` — photo asset.
- `.github/workflows/build-and-release.yml` — CI: on `vX.Y.Z` tag push, compiles the tex and publishes `cv-maldini.pdf` as a GitHub Release asset.
- `.vscode/settings.json` — LaTeX Workshop build recipe, mirrors CI (`pdflatex -output-directory=..`, build on save).

## Build

Local (VSCode + LaTeX Workshop, via `.vscode/settings.json`) or CI both compile `src/cv-maldini.tex` with `-output-directory=..`, so `cv-maldini.pdf` and aux files (`.aux .log .out .synctex.gz`) land at the repo root. All of these are gitignored — **never commit the built PDF or aux files**. The only PDF that matters lives in GitHub Releases.

## Versioning / release flow

No commit-based releases. To publish a new CV version:
1. Edit `src/cv-maldini.tex`, commit, push to `main`.
2. Tag with semver (`git tag v1.2.3 && git push origin v1.2.3`).
3. CI builds and attaches the PDF to a new GitHub Release automatically.

## Editing conventions

Content changes go directly in `src/cv-maldini.tex`. Don't restructure the template/layout unless asked — it's borrowed (LuxSleek-CV), and template changes should stay minimal and deliberate.
