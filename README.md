# PromptLux — web

The public web presence of **PromptLux** (iOS prompt vault + Visual Prompt Deck keyboard).
Static HTML, no build step, hosted on GitHub Pages.

| Page | Purpose |
|---|---|
| `index.html` | Landing page (live since 2026-09-14; promptlux.app since 2026-09-21) |
| `support.html` | **App Store Support URL** — support address, FAQ, § 5 ECG Impressum (`#impressum`) |
| `privacy.html` | **App Store Privacy Policy URL** — "Data Not Collected", keyboard privacy rules, full German statement |
| `THIRD_PARTY_NOTICES.txt` | Lucide (ISC) and Feather (MIT) licence texts for the deck glyphs |
| `robots.txt`, `sitemap.xml`, `404.html` | Crawl hints and the not-found page |

## Addresses

- Canonical: `https://promptlux.app/` (since 2026-09-21; HTTPS enforced by GitHub Pages, Let's Encrypt certificate renewed by GitHub)
- History: `https://promptwhisker.com/` (2026-09-19 → 09-21), `https://promptfox.psystream.net/` (2026-09-14 → 09-19) and `https://winzmiau.github.io/promptfox-web/` — all retired, **no redirects** (decision 2026-10-18: promptlux.app is the only address; the old domains may be reused for other purposes). Old links simply stop working

Support mail: `promptfox@psystream.net` (iCloud+ custom domain; DNS on Cloudflare).

## Updating

Edit a file on github.com (pencil icon) or commit and push. Pages redeploys in about a minute.
The three page names (`index`, `support`, `privacy`) never change once submitted — edit the pages, never rename them. The host may move (it did twice); App Store Connect must then be updated to the new URLs.

## Custom domain (promptlux.app — set up 2026-09-21; the 09-14/09-19 recipes are superseded)

1. Cloudflare → promptlux.app → DNS → Records, proxy **off** (grey cloud): **A** `@` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 and **AAAA** `@` → 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153 (apex domain — GitHub Pages needs A/AAAA, not a CNAME). Optional `www` CNAME → `winzmiau.github.io`.
2. Push this repo with `CNAME` = `promptlux.app`; GitHub → Settings → Pages shows the custom domain; tick **Enforce HTTPS** once the certificate is issued (minutes to an hour). `.app` is HSTS-preloaded, so the site only works over HTTPS — expected.
3. The `CNAME` file must stay. No redirect rules on the old zones — the old addresses are retired, not forwarded.

## Rules

- Everything here is public. No drafts, no secrets, no internal notes.
- Every statement about the app must be true of the shipped build. Source of truth: the app repo's
  `RELEASE_CHECKLIST.md` and `APP_STORE.md`.
- Keep the three page names stable; App Store Connect points at them.
