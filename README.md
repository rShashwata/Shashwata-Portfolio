# Shashwata Roy — Resume Site (Cloudflare Pages)

Static, dependency-free site optimized for Cloudflare Pages.

## Deploy

**Option A — Direct upload (fastest)**
1. Cloudflare Dashboard → Workers & Pages → Create → Pages → Upload assets.
2. Drag the entire contents of this folder (or a zip of it) in.
3. Deploy. Done.

**Option B — Git integration**
1. Push these files to a GitHub/GitLab repo.
2. Cloudflare Pages → Connect to Git → pick the repo.
3. Build settings: **Build command:** (leave empty) · **Build output directory:** `/` (or the folder holding index.html).
4. Deploy.

## Custom domain
Pages project → Custom domains → add `shashwataroy.com` / `www.shashwataroy.com` and follow the DNS prompts. HTTPS is automatic.

> After setting the real domain, update the absolute URLs in
> `index.html` (`og:image`, `twitter:image`, `canonical`),
> `robots.txt`, and `sitemap.xml` if it differs from shashwataroy.com.

## What's included / optimized
- Self-hosted Poppins (latin subset, 4 weights ~8 KB each) — no Google Fonts call.
- Profile photo as WebP (~15 KB) with JPEG fallback (~29 KB), sized 2×.
- Minified HTML + CSS, single file, zero JS.
- `_headers`: security headers + 1-year immutable caching for /assets, no-cache for HTML.
- Branded `404.html`, `robots.txt`, `sitemap.xml`, SVG favicon + apple-touch-icon.
- All hyperlinks from the original PDF preserved and clickable.

Total payload for a first visit: ~60–70 KB.
