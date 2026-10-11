# Lex's Word Quest: website version (build 202610110446)

## What's in this folder
- `index.html`: the game itself (menus, maps, battles, art, music, interface translations).
- `data/<language>.js`: the words, sentences and examples for one language
  (zh = Chinese, ja = Japanese, ko = Korean, vi = Vietnamese, es, de, fr, it, he, ru).
  A player only downloads the language they choose.
- `data/meanings-<zh|ja|ko|vi>.js`: word meanings in Chinese, Japanese, Korean or Vietnamese.
  Only downloaded by players who switch the game language to one of these.

## How to publish
1. Upload the whole folder to the web server, keeping the structure exactly as it is
   (`index.html` next to the `data` folder). Any static web host works; no database or server code is needed.
2. Point the game's page or link at `index.html` (it can also be renamed, e.g. to `word-quest.html`,
   as long as it stays in the same folder as `data/`).
3. Make sure gzip (or brotli) compression is on for `.html` and `.js` files. Most hosts do this automatically.
4. Updating later: replace `index.html` and the `data` folder with the new build. Each build adds a version
   number to the data links, so players automatically get the new files and old cached copies are not used.

## Notes for whoever maintains the site
- Player progress is saved in each player's browser (localStorage), keyed to the website's domain.
  Keep the game on the same domain and path between updates, or players will lose their saves.
- The "Friends of LTL" shared characters only work on the claude.ai version. On the website they are stored on the player's device.
- The tab icon (Lex the Lion) is built into `index.html`.
