# Lex's Word Quest: website version (build 202610200840)

## What's in this folder
- `index.html`: the game itself (menus, maps, battles, art, music, interface translations).
- `data/<language>.js`: the words, sentences and examples for one language. A player only downloads the language they choose.
- `data/meanings-<zh|ja|ko|vi>.js`: word meanings in Chinese, Japanese, Korean or Vietnamese, only downloaded by players who switch the game language.

## How to publish
1. Upload the whole folder to the web server, keeping `index.html` next to the `data` folder. Any static web host works.
2. Make sure gzip (or brotli) compression is on for `.html` and `.js` files.
3. Updating later: replace `index.html` and the `data` folder with the new build. Each build adds a version number to the data links, so players get the new files.

## Notes
- Player progress is saved in each player's browser, keyed to the website's address. Keep the game on the same address between updates.
- Save IDs, Friends of LTL, problem reports and player statistics use the Cloudflare Worker at https://lex-saves.zhaofengoffice.workers.dev.
