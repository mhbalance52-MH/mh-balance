# M H Balance — Corporate Website

A static, single-page bilingual (Arabic/English) corporate website for M H Balance.

## Structure

```
index.html          the entire site (HTML + CSS + JS in one file)
assets/
  logo.png           brand logo, transparent background
  favicon.png         browser tab icon
README.md
```

## Language

- Arabic (RTL) is the default language on first visit.
- The visitor's language choice is remembered (via `localStorage`) once they switch to English, so returning visitors keep their preference.
- Switching is handled entirely client-side in the `<script>` block at the bottom of `index.html` — no build step, no server.

## Font

The brand font is **Sakkal Majalla**. It is *not* loaded from a remote source — it's a font commonly bundled with Windows/Office, so no external font request is made and nothing can break on deployment. Where a visitor's device doesn't have it installed, the site falls back to a close system serif (different fallback stacks for Arabic and English are defined in the CSS as `--font-family-primary`). If you later obtain a licensed web-font file for Sakkal Majalla, add it under `assets/fonts/` and register it with `@font-face` at the top of the `<style>` block.

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `m-h-balance`).
2. Upload `index.html` and the `assets/` folder to the repository root — keep them in the same relative locations (`assets/logo.png`, `assets/favicon.png`), since the HTML references them with relative paths.
3. In the repository settings, open **Pages**, set the source branch (usually `main`) and root folder (`/`), and save.
4. GitHub will publish the site at `https://<username>.github.io/<repository-name>/`.

No build tools, backend, or database are required — this is a fully static site.

## Contact information on the site

- Phone / WhatsApp: `01041930453`
- Email: `mhbalance52@gmail.com`
- Facebook and Instagram: linked via icon buttons in the contact section and footer

To update any of these, search `index.html` for the value you want to change — each one appears in a small number of places (nav, hero, CTA, contact section, footer) and is easy to find with your editor's search function.
