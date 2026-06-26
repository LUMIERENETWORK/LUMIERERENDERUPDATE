# LUMIERE RENDER — Update Channel

This repository is the **public distribution channel** for the LUMIERE RENDER tool's
auto-update system. It contains **only**:

- `version.json` — the latest version number, download URL, and release notes.
- GitHub Releases — each release hosts `LUMIERE_RENDER.zip` (the built application).

**No source code is published here.** The application source lives in a private repository.

## How auto-update works

1. On launch, the app reads `version.json` from this repo's `main` branch.
2. If the published `version` is newer than the installed one, the app downloads the
   `LUMIERE_RENDER.zip` from the latest Release.
3. An external updater swaps the files and restarts the app.

## Publishing a new version

1. Bump `version` in `version.json` and update `notes`, then commit/push to `main`.
2. Build `LUMIERE_RENDER.zip` and attach it to a new GitHub Release.
