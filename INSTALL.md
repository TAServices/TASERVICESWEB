# T&A Services — Redesign Drop-In Package

## What's in this zip
```
index.html               → replaces repo root /index.html
styles.css                → replaces repo root /styles.css
contact/index.html        → replaces /contact/index.html
services/index.html       → replaces /services/index.html
water-damage/index.html   → replaces /water-damage/index.html
```

## How to install (GitHub.com, no git needed)
For each file above:
1. Open the matching file in your repo (e.g. `contact/index.html`)
2. Click the pencil (edit) icon
3. Select all, delete, paste in the new file's contents
4. Commit directly to `main`

Repeat for all 5 files. Takes about 5 minutes.

## Files to delete from the repo (no longer used)
These belonged to the old design and aren't referenced anywhere anymore:
- `style.css` (note: singular — different from `styles.css`, which you're keeping)
- `ta-mobile-fixes.css`

Leave everything else as-is: `CNAME`, `robots.txt`, `sitemap.xml`, `README.md`,
`TAServiceWEB`, and the whole `assets/` folder (logo, favicons, gallery photos)
don't need any changes.

## What changed
- One consistent navy + safety-orange design across the homepage AND all three
  subpages (contact, services, water-damage) — previously each subpage had its
  own unrelated teal/yellow inline styles.
- Fixed a photo-cropping bug on the Water Damage service card: the thumbnail
  box now matches the photo's actual 4:3 aspect ratio instead of forcing a
  fixed-height crop that cut into the image at a random angle.
- Real content (FAQs, schema/JSON-LD, service-area copy) from the original
  water-damage page is fully preserved — only the visual shell changed.
- Buttons now pass WCAG AA contrast (4.5:1) for their text.

## After you push
Hard-refresh any page you check (Ctrl+Shift+R / Cmd+Shift+R) — browsers cache
CSS aggressively, so you may see the old look until you force a reload.

## One thing worth doing yourself
The Mold Remediation and Weather Damage service cards currently use a
branded gradient + icon instead of a real photo (no confirmed real job photos
for those categories were available). If you have real before/after shots,
swap them in — look for `.thumb.mold` and `.thumb.weather` in `index.html`
and `services/index.html`, and follow the same pattern used for
`.thumb.water` (a `background-image:url(...)` inline style pointing at
`/assets/...`).
