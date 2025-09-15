# T&A Services — Static Website (Formspree enabled)

This folder contains a static site (`index.html` + `styles.css`) with **Formspree** wired in via AJAX.

## Formspree endpoint
Already set to:
```
https://formspree.io/f/mandzqlj
```
You can change it anytime by editing the `action` attribute on both forms in `index.html`.

## Quick preview
Open `index.html` in your browser. For a local server:
```
python3 -m http.server 5500
```

## Deploy to GitHub Pages
1. Push these files to `https://github.com/TAServices/TASERVICESWEB` (root of the repo).
2. Repo **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / **/** (root) → **Save**.
3. Your project URL: `https://TAServices.github.io/TASERVICESWEB/`

## Custom domain
A `CNAME` file sets `www.TAWaterServices.com`. After pushing, enable **Enforce HTTPS** in **Settings → Pages**.

## DNS (Namecheap)
- CNAME `www` → `TAServices.github.io`
- A `@` → `185.199.108.153`
- A `@` → `185.199.109.153`
- A `@` → `185.199.110.153`
- A `@` → `185.199.111.153`

## Files
- index.html — two forms posting to Formspree via fetch()
- styles.css
- CNAME — sets custom domain to `www.TAWaterServices.com`
