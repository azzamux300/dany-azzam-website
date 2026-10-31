# Dany Azzam website – how to edit

Static site, no build step. GitHub Pages deploys `main` automatically to danyazzamcars.com.

## Add a car
1. Save photos to `cars/<new-slug>/01.jpg, 02.jpg, …` (EXIF-rotated, fit in 900x1200, JPEG q76 progressive). Best front 3/4 exterior first, then exterior angles, close-ups, interior. Never reuse a slug.
2. Add an entry at the top of `const CARS=[` in `index.html`:
   `{name, trim, year, price, mi, km, color:{ar,en}, interior:{ar,en}, engine, gear:{ar,en}, kw, photos:pics("<slug>", <count>), feats:{ar:[…],en:[…]}}`
   - price/mi/km are plain numbers; km = miles × 1.609344 rounded to 100.
   - Arabic in simple Lebanese wording. `kw` = extra search words incl. Arabic spellings.
3. Check the script parses, commit, push to `main`.

## Sold / price change
- Sold: delete the car's entry from `CARS` and its `cars/<slug>/` folder.
- Price: change `price` only.

## Fixed details
Phone/WhatsApp +961 70 228 556 · Instagram @danyazzamcars4all_ · TikTok @danyazzamcars4all · Location: Mirna El Chalouhi Highway, after Gallery El Ittihad.
