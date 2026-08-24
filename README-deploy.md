# Getting this online, free, in about five minutes

This folder is the whole site. One HTML file plus images — no build step, no
dependencies, nothing to install.

```
index.html          the site
og-cover.png        link-preview image (LinkedIn, WhatsApp, Slack)
favicon-32.png      browser tab icon
favicon-512.png     spare, larger version
logo-mz-brass-transparent.png   spare monogram
cv.pdf              ← you add this
```

---

## Option A — Cloudflare Pages (easiest, no git)

1. Sign up free at **dash.cloudflare.com** → **Workers & Pages** → **Create**
   → **Pages** → **Upload assets**.
2. Name the project, e.g. `moayid-zaidi`. That name becomes your URL:
   `moayid-zaidi.pages.dev`.
3. Drag this whole folder onto the upload area. Click **Deploy site**.
4. Done — the URL is live with HTTPS.

To update anything later, drag the folder again — it redeploys to the same URL.

Free plan gives you unlimited requests and bandwidth, 500 builds a month, and
up to 20,000 files. This site is six.

## Option B — GitHub Pages (if you'd rather it live in a repo)

1. Create a public repo named exactly `<your-username>.github.io`.
2. Upload the contents of this folder to the repo root.
3. **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save.
4. Live at `https://<your-username>.github.io` within a minute or two.

Free for public repos, HTTPS included.

---

## Before you share the link

1. **Add your CV.** Drop it into this folder named exactly `cv.pdf` — two
   buttons on the page point at it.
2. **Fix the link preview.** In `index.html`, set `og:url` to your real URL and
   `og:image` to the full absolute URL of the cover image, e.g.
   `https://moayid-zaidi.pages.dev/og-cover.png`. Without the absolute URL,
   LinkedIn shows a bare link instead of a preview card.
3. **Fill in the outcomes.** Every highlighted italic passage on the page is a
   placeholder — mostly the "Outcome" column of each case study. These are the
   most valuable sentences on the site and the only ones I couldn't write for
   you. Search the file for `class="todo"` to find them all.
4. **Add the years** to the two case-study role lines.

## Swapping the images for your originals

Right now the nine project screenshots and your portrait load directly from
your Google Site. They work, but Google can invalidate those URLs if you edit
or remove the images there — so treat it as temporary.

When you have ten minutes: make an `img` folder here, save your originals into
it, and replace each `src="https://lh3.googleusercontent.com/..."` with
`src="img/your-file.png"`. Every one is marked with a `SWAP` comment.

Export at roughly 1400px wide as PNG for UI screens. Your portrait wants to be
about 800×1000.

## A note on the image captions

I reassigned the nine screenshots between the two case studies based on what
each one shows — the record and dashboard screens with the data-replication
work, the login and evaluation screens with the Moodle integration. If I've put
any of them with the wrong project, move the `<figure>` block; the captions are
written to be rewritten.

## Custom domain, later

Both hosts support custom domains free — you only pay for the domain itself
(around $12/year for a `.com`). Cloudflare Pages: project → Custom domains.
GitHub Pages: Settings → Pages → Custom domain. Do this once you're happy with
the content; the free subdomain is perfectly respectable in the meantime.
