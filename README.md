# PromptFox — web

The public web presence of **PromptFox** (iOS prompt vault + Visual Prompt Deck keyboard).
Static HTML, no build step, hosted on GitHub Pages.

| Page | Purpose |
|---|---|
| `index.html` | Landing page (live since 2026-09-14) |
| `support.html` | **App Store Support URL** — support address, FAQ, § 5 ECG Impressum (`#impressum`) |
| `privacy.html` | **App Store Privacy Policy URL** — "Data Not Collected", keyboard privacy rules, full German statement |
| `THIRD_PARTY_NOTICES.txt` | Lucide (ISC) and Feather (MIT) licence texts for the deck glyphs |
| `robots.txt`, `sitemap.xml`, `404.html` | Crawl hints and the not-found page |

## Addresses

- Canonical: `https://promptfox.psystream.net/` (live since 2026-09-14, HTTPS enforced, Let's Encrypt certificate renewed by GitHub)
- Old address `https://winzmiau.github.io/promptfox-web/` redirects (301) to the canonical one

Support mail: `promptfox@psystream.net` (iCloud+ custom domain; DNS on Cloudflare).

## Updating

Edit a file on github.com (pencil icon) or commit and push. Pages redeploys in about a minute.
The two store URLs never change once submitted — edit the pages, never rename them.

## Custom domain (set up 2026-09-14 — for reference if it ever needs redoing)

1. Cloudflare → psystream.net → DNS → Records → Add: **CNAME** `promptfox` → `winzmiau.github.io`, proxy **off** (grey cloud).
2. GitHub → this repo → Settings → Pages → Custom domain `promptfox.psystream.net` → Save; tick **Enforce HTTPS** once the certificate is issued (a few minutes).
3. The `CNAME` file GitHub writes to this repo must stay.

## Rules

- Everything here is public. No drafts, no secrets, no internal notes.
- Every statement about the app must be true of the shipped build. Source of truth: the app repo's
  `RELEASE_CHECKLIST.md` and `APP_STORE.md`.
- Keep the three page names stable; App Store Connect points at them.
