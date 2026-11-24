# Times Table Bakery

A one-page web app that teaches multiplication and division to 6 to 8 year olds with trays of cookies.

- **How it works:** picture lessons. `3 × 4` means 3 rows of 4. `12 ÷ 3` means 12 shared by 3.
- **Daily puzzles:** a Times bake and a Sharing bake, 4 short steps each. Each one earns a sticker on a 7-day chart. The same date and level always give the same puzzle.
- **Cookie Rush:** a quick-fire game with two modes. **No timer** (the default) is 10 questions with no clock and no speed points, for starters. **60 seconds** gives bonus points for faster right answers. In both, wrong answers never lose points, and missed facts come back later in the round.
- **Giant tray:** free play on a 20 × 20 grid that shows the times and sharing facts for any rectangle.
- **Levels:** tables 2, 5, 10, then 2, 3, 4, then 6 to 9.

## Run it

Open `index.html` in any browser. There is no build step and no server.
It loads the Fredoka and Nunito fonts from Google Fonts, and falls back to system fonts when offline.

Stickers, the streak and best scores are saved in the browser's `localStorage`, on that device only.
