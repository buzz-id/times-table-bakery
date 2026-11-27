# Times Table Bakery

A one-page web app that teaches multiplication and division to 6 to 8 year olds with trays of cookies.
It works without wifi once it has been opened online.

- **How it works:** picture lessons. `3 × 4` means 3 rows of 4. `12 ÷ 3` means 12 shared by 3.
- **Daily puzzles:** a Times bake and a Sharing bake, 4 short steps each. Each one earns a sticker on a 7-day chart. The same date and level always give the same puzzle.
- **Cookie Rush:** a quick-fire game with two modes. **No timer** (the default) is 10 questions with no clock and no speed points, for starters. **60 seconds** gives bonus points for faster right answers. In both, wrong answers never lose points, and missed facts come back later in the round.
- **Giant tray:** free play on a 20 × 20 grid that shows the times and sharing facts for any rectangle.
- **Levels:** tables 2, 5, 10, then 2, 3, 4, then 6 to 9.

## Play offline

1. Open the site once while online: https://buzz-id.github.io/times-table-bakery/ (GitHub Pages must be turned on for this repository).
2. Wait for the line at the bottom of the page: "Saved on this device. Times Table Bakery now works without wifi."
3. Optional: add it to the home screen so it opens like an app.
   - iPad or iPhone (Safari): Share, then **Add to Home Screen**.
   - Android (Chrome): menu, then **Install app** or **Add to Home screen**.

After that it opens and plays fully without a connection. When the device is online again, it picks up any new version automatically.

Stickers, the streak and best scores are saved on the device, in the browser's `localStorage`.
On an iPad or iPhone, the home-screen app keeps its own progress, separate from Safari, so pick one and stick with it.

## How it is built

| File | What it is |
|---|---|
| `src/bakery.html` | The page itself. Edit this one. It is also the version published on claude.ai. |
| `build.py` | Turns `src/bakery.html` into `index.html` and `sw.js`. |
| `index.html` | The built page. It uses the fonts in `fonts/` instead of Google Fonts. |
| `sw.js` | The service worker that saves the app for offline play. Built, do not edit. |
| `manifest.webmanifest`, `icons/` | Name and icons for "Add to Home Screen". |
| `fonts/` | Fredoka and Nunito (SIL Open Font License, see the `OFL-*.txt` files). |

After changing `src/bakery.html`, rebuild and commit `index.html` and `sw.js` with it:

```bash
python3 build.py
```

The service worker's cache name changes whenever a saved file changes, so devices replace their old copy.

Opening `index.html` straight from a folder (a `file://` address) also works, but offline saving only switches on when the page is served from a website such as GitHub Pages.
