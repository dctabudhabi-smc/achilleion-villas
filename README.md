# Achilleion Villas — Property Sales Site

A single-page, cinematic sales site for two villas in Gastouri, Corfu.

## Structure
```
index.html            ← the whole site (images embedded; ready to open)
assets/video/
  hero.mp4            ← homepage background film (muted loop)
  elizabeth.mp4       ← Villa Elizabeth film
  sissy.mp4           ← Villa Sissy film
```

## Deploy on GitHub Pages
1. Create a repo and upload the **entire folder contents** (keep `index.html` and the `assets/` folder side by side).
2. Repo → **Settings → Pages** → Source: `main` branch, `/root`.
3. Your site goes live at `https://<username>.github.io/<repo>/`.

That's it — no build step. The photos are baked into `index.html`; only the three videos load from `assets/video/`.

## Things you'll likely want to edit (all in `index.html`)
- **Contact details** — currently placeholders (Alexandra Stephanou / sales@achilleionvillas.com / +30 …). Search the file for `id="enquire"`.
- **Enquiry form** — it currently shows a thank-you message on submit but does not send anywhere. Wire it to Formspree/Getform or your inbox when ready.
- **Golden Visa link** — points to enterprisegreece.gov.gr; swap for your preferred source.
- **The land wording** — phrased as "a share of 2,000 m² adjoining land" per villa; adjust if the parcel/licence is structured differently.

## Social sharing (WhatsApp / Facebook / LinkedIn / X) — one required edit
Open `index.html`, find the **SOCIAL SHARING** comment block in the `<head>`, and replace
`https://achilleionvillas.com/for-sale/` with the **live URL where you host the site**
(e.g. your GitHub Pages URL). The `og:url`, `og:image`, `canonical` and Twitter tags all use it.
These must be absolute URLs or link previews won't show the image.
- Share image: `assets/og-image.jpg` (1200×630, the sunset shot)
- Favicons: `assets/favicon.ico`, `favicon.png`, `favicon-32.png`, `apple-touch-icon.png`
After deploying, you can validate the preview at developers.facebook.com/tools/debug or by pasting the link into a WhatsApp chat to yourself.
