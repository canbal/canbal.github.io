# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Personal one-page website for Can Bal, served by GitHub Pages at https://canbal.me (custom domain via `CNAME`). Forked from [timothygebhard/minimal-academic-website](https://github.com/timothygebhard/minimal-academic-website).

Pure static HTML/CSS. There is no build step, package manager, linter, or test suite. Pushing to `main` deploys.

## Commands

Preview locally:

```
python -m http.server 8000
```

Then open http://localhost:8000.

## Structure

- `index.html` — all content. Small uppercase `<h2>` labels (These days / Before that / Investing / Outside work) break up left-aligned paragraphs inside `<main id="content">`; social links are the `<ul class="icons">` list at the bottom. `<head>` carries a meta description and Open Graph tags for link previews.
- `main.css` — all styling. `#content` is a centered 600px column. The avatar and name are centered; body text and section labels are left-aligned. Keep the copy casual and conversational, not résumé-speak.
- `image.jpg` (avatar) and `favicon.png` are the only assets.

## Things to know before editing

- Third-party CSS (Font Awesome 6.1.1, Academicons 1.9.2) is loaded from cdnjs with SRI `integrity` hashes. Bumping a version requires updating the matching hash or the stylesheet will be blocked.
- The font is Source Sans Pro from Google Fonts, weights 300 and 600 only. Using another weight in CSS requires adding it to the Google Fonts URL.
- The mailto link uses `hi - at - canbal.me` on purpose as spam obfuscation. Do not "fix" it into a real address.
- Icons come from two sets: `fas`/`fab` classes are Font Awesome, `ai ai-*` classes are Academicons.
