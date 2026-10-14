# CR Telecom — website package (v2)

## Files (upload ALL to the same web root)
- index.html            the whole site (HTML + CSS + JS in one file, no build step)
- favicon.svg           primary icon (sharp at any size)
- favicon.ico           legacy fallback (16/32/48)
- favicon-16x16.png, favicon-32x32.png, favicon.png (128px)
- apple-touch-icon.png  iPhone/iPad home screen (180px)
- icon-192.png, icon-512.png, site.webmanifest   Android / installable app icons

## Preview locally
  python -m http.server 8000     then open http://localhost:8000
(Opening index.html directly also works.) Fonts load from Google Fonts; the site
falls back to system fonts if they are blocked.

## Deploy
Netlify / Cloudflare Pages / GitHub Pages / any static host. No build command.

## Edit before launch (top of the <script> in index.html)
  CONFIG.CONTACT_EMAIL  placeholder hello@crtelecom.com — set your real inbox
  CONFIG.LEAD_ENDPOINT  URL that accepts a JSON POST (Formspree, Netlify Forms, your API).
                        Empty = the form opens the visitor's email app instead.
  CONFIG.CONSOLE_URL    your customer console URL. Empty = Login opens "request access".
  RATES                 Meta India list rates used by the WhatsApp fee estimator.
                        Re-check against Meta's current rate card before launch.

## Pages you still need to create
  privacy.html and terms.html (linked from the footer and the form consent line).

## Claims to verify or remove before accepting customers
- "24/7 support" in the hero.
- Product capabilities described in the channel panels (IVR languages, number masking,
  carousels, fallback routing, sandbox, shared inbox, etc.) — keep only what you can deliver.
- The API in the Developers section is illustrative (api.crtelecom.com does not exist yet).
- Dashboard numbers, chart, live feed, fallback timings are SAMPLE data and are labelled so.
- Compliance copy reflects TRAI/DLT, 140/1600-series, Meta and RCS rules as of Oct 2026.
  Rules change; have your compliance lead review the "Launch compliant" section.
- Add your company legal name, registered address, and any TRAI/DoT registrations to the footer.
- Do not add customer logos, uptime/delivery percentages or certifications until real.
- WhatsApp logo/brand use: follow Meta's brand guidelines; the icons here are generic.
- Replace the header logo mark with your full brand logo SVG when available
  (the CR monogram here matches the new favicon).

## Not connected (needs real engineering)
Authentication, accounts, provider/carrier APIs, provisioning, metering, billing,
API keys, lead storage, consent/privacy flows, monitoring.
