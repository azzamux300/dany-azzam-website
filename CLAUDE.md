# Dany Azzam website – how to edit

Static site, no build step. GitHub Pages deploys `main` automatically to danyazzamcars.com.

## Add a car
1. Save photos to `cars/<new-slug>/01.jpg, 02.jpg, …` (EXIF-rotated, fit in 900x1200, JPEG q76 progressive). Best front 3/4 exterior first, then exterior angles, close-ups, interior. Never reuse a slug.
2. Add an entry at the top of `const CARS=[` in `index.html`:
   `{name, trim, year, price, mi, km, color:{ar,en}, interior:{ar,en}, engine, gear:{ar,en}, kw, photos:pics("<slug>", <count>), feats:{ar:[…],en:[…]}}`
   - price/mi/km are plain numbers; km = miles × 1.609344 rounded to 100.
   - Arabic in simple Lebanese wording. `kw` = extra search words incl. Arabic spellings.
3. Check the script parses, commit, push to `main`.

## Sold / on the way / price change
- Sold: add `sold:true` to the car's entry. It shows greyed out with a "Sold" label at the end of the collection and drops off the home page. After a few weeks, delete the entry and its `cars/<slug>/` folder.
- On the way (bought, still shipping): add `soon:true`. It shows an "On the way" label and the WhatsApp button becomes "Reserve". Remove `soon` when the car arrives.
- Price: change `price` only.

## Car links
Each car has its own link: `danyazzamcars.com/#car/<slug>` (the slug is its photo folder name). Renaming a car's folder breaks links already shared, so don't.

## Fixed details
Phone/WhatsApp +961 70 228 556 · Instagram @danyazzamcars4all_ · TikTok @danyazzamcars4all · Location: Mirna El Chalouhi Highway, after Gallery El Ittihad.
