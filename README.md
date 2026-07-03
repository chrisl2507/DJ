# DJ Stanway Personal Training — Website

Single-page marketing site for **David-John (DJ) Stanway**, personal trainer in
Ipswich, Suffolk — Hyrox competition prep, diabetes-friendly coaching and 1:1
personal training. ([@djstanwaypt_](https://www.instagram.com/djstanwaypt_/))

Pure static HTML/CSS/JS — no build step, no dependencies.

```
index.html        all page markup
css/style.css     all styles (design tokens at the top in :root)
js/main.js        mobile nav, scroll animations, stat counters, contact form
assets/           favicon (add real photos here too)
```

## Run locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser.

## Deploy

Any static host works as-is:

- **GitHub Pages** — repo Settings → Pages → deploy from branch.
- **Netlify / Vercel / Cloudflare Pages** — point at the repo, no build command,
  publish directory = repo root.

## Placeholders to swap before launch

Everything marked `PLACEHOLDER` in `index.html` comments:

| What | Where | Swap with |
|---|---|---|
| Hero photo | `.hero__media` | `<img src="assets/hero.jpg" ...>` — portrait, ~4:5 (DJ mid-session) |
| About photo | `.about__media` | `<img src="assets/about.jpg" ...>` — portrait, ~3:4 |
| Stats numbers | `#stats` section, `data-count` attributes | DJ's real figures (years coaching, events, clients) |
| Credentials | `.about__chips` list | DJ's actual qualifications |
| Testimonials | `#results` section | Real client quotes, with permission |
| Instagram tiles | `.insta__grid` | Real post images (each tile links to the profile) |
| Email | `mailto:hello@djstanwaypt.co.uk` | DJ's real email address |
| Phone | `tel:+447000000000` | DJ's real number |

## Activating the contact form

The form posts to Formspree but ships with a placeholder endpoint (until then it
shows a friendly "DM on Instagram instead" message rather than failing):

1. Create a free form at [formspree.io](https://formspree.io) (50 submissions/month free).
2. Copy the form ID and replace `YOUR_FORM_ID` in the `action` attribute of
   `#contact-form` in `index.html`.

## Design tokens

Colours, fonts and sizing live in `:root` at the top of `css/style.css` —
change `--accent` there to re-theme the whole site.
