# Aminco Group Website

A single-page site for Aminco Group covering three service lines:

- **Queen Sheba Honey** — premium Yemeni Sidr honey
- **Aminco Mobile Car Wash** — Uptown Cairo Compound
- **Kingdom of Aminco** — truck transportation

## Project structure

```
.
├── index.html   # the entire site — HTML, CSS, and JS in one file, no build step
└── README.md
```

This is a **static, dependency-free site**. There is no build process, no
package manager, and no external JS libraries — everything (fonts aside)
is self-contained in `index.html`. The only external network calls are to
Google Fonts (`fonts.googleapis.com` / `fonts.gstatic.com`) for the
Fraunces and Inter typefaces.

## Running it locally

Just open `index.html` directly in a browser, or serve it with any static
file server, e.g.:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Current functionality

- Sticky top navigation (desktop) and a fixed bottom tab bar (mobile) to
  jump between the three service sections
- An "Order / Book / Request Quote" button under each service that opens
  a JavaScript `confirm()` precaution step before proceeding, to help
  prevent order/shipping mistakes
- These buttons are currently wired to a **placeholder WhatsApp number**
  (`201000000000`) in the `href` attributes and are styled as "coming
  soon" until a real number is supplied — search the file for
  `wa.me/201000000000` and `number coming soon` to find every place this
  needs updating
- Color palette and logo mark are placeholders reflecting Aminco Group's
  brand board; the honey section's crowned-bee mark is embedded as a
  base64 PNG cropped from a marketing render (not a vector file)

## Deploying to GitHub

1. Unzip this project locally.
2. From inside the project folder:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Aminco Group website"
   ```
3. Create a new empty repository on GitHub (no README/license, to avoid
   merge conflicts with the commit above).
4. Connect and push:
   ```bash
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git branch -M main
   git push -u origin main
   ```

## Connecting to Bolt.new

Once the repo is on GitHub, in Bolt.new choose the "Import from GitHub"
option and paste the repository URL. Since this is a plain static
HTML/CSS/JS project with no build tooling, Bolt.new will be able to open
and run it directly without any additional configuration.
