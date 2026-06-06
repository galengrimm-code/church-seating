# Pew Planner

A free, single-file church seating chart tool — assign families and guests to specific
seats at church events (funerals, weddings, special services) and print the result for ushers.

No accounts, no database, no internet required. Open the file in a browser and go.
Everything you enter stays on your own device.

## Use it

Open `index.html` in any modern browser (Chrome, Edge, Safari, Firefox). That's the whole
install. To put it on a wall or hand it to ushers, use **Print**.

### Three steps

1. **Type a family or guest name** in the big box at the top. A colored dot shows the color
   they'll get on the map.
2. **Click their seats.** Each fills with their color and shows their initials. Click as many
   as the family needs.
3. **Type the next name and repeat.** Every family automatically gets a distinct color.

Click an assigned seat again to clear it.

## Features

- **Visual seating map** — 14 pews per side, 10 seats each, with an aisle and altar area.
- **Folding chairs** — optional "extra chairs" at row ends, drawn as actual folding chairs so
  they're easy to tell apart from pews. Toggle in **Options**.
- **Multiple charts** — save a separate chart per event. New / Open / Duplicate / Rename /
  Delete from the **Charts** panel. Your work auto-saves to the browser as you go.
- **Automatic, readable colors** — each family gets a unique color; initials switch between
  dark and light automatically for contrast.
- **Print** — full visual map for the wall, or a compact pocket list (check "Pocket-size
  print" in Options first).
- **Backup & share** — Export a lossless `.json` backup, or a `.csv` you can open in a
  spreadsheet or email. Import either one back in.
- **Accessible** — seats are real buttons; keyboard and screen-reader friendly.

## Privacy

This tool runs entirely in your browser. Names you enter are saved only in that browser's
local storage and are never uploaded anywhere. Clearing your browser data, or using a
different device, starts fresh — use **Export** to move a chart between devices.

## Tech notes

- One self-contained `index.html`. No build step, no dependencies, no backend.
- The only external request is Google Fonts (Cinzel + Lato); the tool works offline without
  them, just with system fonts.
- State is structured behind a small storage adapter, so a hosted/multi-user version backed
  by a database could be added later without rewriting the app.

## License

[MIT](LICENSE) — free to use, modify, and share.
