# We the People — Campaign in a Box

Static landing page for `wethepeople.gingeralchemy.com`.

A research-backed campaign website offer for first-time Democratic and independent challengers running in red states. Built and run by Jamie Stephens / Ginger Alchemy LLC.

## Files

- `index.html` — the entire landing page (single-file, no build step)
- `jamie.jpg` — Jamie at #NoKings NWA rally
- `letisha-site.jpg` — Screenshot of letishaforarkansas.com (live example)

## Deploy

Deployed via Vercel as a static site. No build command, no framework. Vercel auto-detects and serves the files as-is.

1. Create new project in Vercel
2. Connect this GitHub repo
3. Framework preset: **Other** (or "Static")
4. Build command: leave blank
5. Output directory: leave blank (root is served)
6. Add custom domain: `wethepeople.gingeralchemy.com`
7. CNAME record at Squarespace: `wethepeople` → `cname.vercel-dns.com`

## Forms + payments

The intake form posts to Formspree (`xaqvdnon`). On successful submission, JavaScript redirects the user to the Stripe deposit checkout (`buy.stripe.com/8x2eVc78takPbBjftqgfu02`) with their email pre-filled. If JS fails, Formspree's `_next` field handles the redirect as a fallback.
