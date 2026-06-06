# Pew Planner — free single-file tool (church-seating)

The free, no-account version of Pew Planner: one self-contained `index.html` for assigning families/guests to church-event seats and printing the result. No backend, no build step, no dependencies (Google Fonts only). State persists in `localStorage`; sharing is via CSV/JSON export. Public repo `galengrimm-code/church-seating`, MIT.

> The full multi-tenant cloud version lives separately at `Documents/Websites/church-seating-app/` (Vite + React + Firebase, in progress).

## Tech Stack

| Layer | Tech |
| ----- | ---- |
| Frontend | Single static `index.html` (vanilla JS + CSS) |
| Backend | None |
| Data | Browser `localStorage`; CSV + JSON export/import |
| Hosting | None deployed (open the file, or clone). Public GitHub repo. |

## Architecture

One file. Fixed layout: 14 benches per side, 10 seats each, two sections + center aisle, with optional folding chairs at row ends. Pews render as continuous benches, folding chairs as distinct chair shapes. Seat keys `side-bench-seat`. All logic inline in the `<script>` block. (Configurable layouts live in the cloud app, not here.)

## Security Notes

- No secrets, no auth, no server, no API routes. Nothing to leak.
- `localStorage` holds event/family names + seat assignments only — no passwords, tokens, or financial data (so not `localstorage-sensitive`).
- No `dangerouslySetInnerHTML`; user-entered names are escaped before render.
- Single file is ~1.2k lines — under the v6.8 1500-line `file-over-500` threshold.

## Common Workflows

- **Run:** open `index.html` in any browser.
- **Deploy:** none yet (could be GitHub Pages / static host).

<!-- SCAN:AUTO:START — managed by Watch Tower scan prompt. Do not edit manually. -->
<!-- SCAN:AUTO:END -->
