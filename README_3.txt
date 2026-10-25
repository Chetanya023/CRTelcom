CR Telecom website  (two verticals)

FILES
  index.html               Products: Voice, SMS, RCS, WhatsApp
  digital-marketing.html   Digital Marketing: SEO, Website building, Ads and social, OBD/IVR
  favicon.svg, favicon.ico, apple-touch-icon.png   browser tab and home-screen icons

Each page is fully self-contained: all styling and scripts are inside the HTML file, so it
displays correctly even if opened on its own. Keep both pages in the same folder so the
Products | Digital Marketing switcher and cross-links work. The icon files are optional
(the tab icon is also embedded in each page).

PREVIEW   Double-click index.html, or run:  python -m http.server 8000
DEPLOY    Upload all 5 files to any static host (Netlify, Cloudflare Pages, GitHub Pages). No build step.

EDIT BEFORE LAUNCH  (search for "CONFIG" near the top of the <script> in BOTH pages)
  CONTACT_EMAIL   placeholder hello@crtelecom.com - set your real inbox
  LEAD_ENDPOINT   URL that accepts a JSON POST (Formspree, Netlify Forms, your API). Empty = the
                  form opens the visitor's email app. Each lead includes "vertical" (products|marketing).
  CONSOLE_URL     your customer console URL. Empty = Login opens "request access".
  index.html only: RATES = Meta India list rates for the WhatsApp fee estimator - re-check before launch.

STILL TO CREATE   privacy.html and terms.html (linked from the footer and the form consent line).

VERIFY BEFORE LAUNCH
  - Every capability described is what you intend to deliver; remove anything you cannot.
  - "24/7 support" (hero) and "you own the domain, hosting and ad accounts" are commitments to confirm.
  - Dashboards, charts, feeds, simulators and planners use SAMPLE data and are labelled so.
  - The API shown in the Developers section is illustrative (api.crtelecom.com does not exist yet).
  - Compliance copy reflects Oct 2026 (TRAI DLT, 140/1600 series, TCCCPR Feb 2025, Meta rates, DPDP Rules).
    Have your compliance lead review it. Add legal name, address and registrations to the footer.

NOT CONNECTED (needs real engineering)
  Accounts and login, carrier/provider APIs, dialer and campaign engine, billing, API keys,
  lead storage/CRM, consent logging, monitoring.
