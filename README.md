
# T&A Services — Mobile Patch (Non-Destructive)

This patch fixes alignment/stacking issues on phones **without** replacing your existing files.

## How to Install
1. **Add the viewport meta** in your `<head>` (if missing):
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1">
   ```
2. **Upload `ta-mobile-fixes.css`** to the root of your site (or your `css/` folder).
3. **Link it *after* your main stylesheet** in `index.html`:
   ```html
   <link rel="stylesheet" href="style.css?v=4">
   <link rel="stylesheet" href="ta-mobile-fixes.css?v=1"> <!-- add this line -->
   ```
   (Change `style.css` to whatever your main CSS file is. The `?v=` cache-bust helps phones pick it up.)
4. **Commit & push**. Then open the site in a Private/Incognito tab on your phone to verify.

## What it fixes
- Lets the header **wrap to two rows** and moves the **Call** button to a full-width row on phones.
- Forces common column classes to **stack to 100% width** at ≤ 767px.
- Adds universal **fluid images** and prevents horizontal scrolling.
- Adds safer **container padding** so content stays aligned on small screens.

## If you still see issues
- You may have components using `position:absolute` or fixed pixel widths. Send me your header HTML (or a link) and I’ll tailor selectors (1:1) with zero redesign.
