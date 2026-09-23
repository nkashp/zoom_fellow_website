# Zoom Fellowship Website

This repo hosts the website for the Zoom Fellowship at ASU's Next Lab — a
hub showcasing the student fellows and the Zoom Apps they're building each
cohort.

---

## What's in this repo

```
zoomWebsite/
  index.html               # Redirects to the main fellows site below
  websites/                 # Static sites (no build step needed)
    nextlab-zoom-fellows/   # Main fellows hub — mentor + cohort project cards
    zoom-momentum-website/  # Landing page for the Zoom Momentum project
    product-page/           # Additional product landing page
  apps/                      # Full application source code for individual
                             # fellow projects (not deployed as part of the
                             # website — see each app's own README)
  docs/                      # Planning notes, status docs, and other
                             # non-website reference material
```

The site you actually browse to is `websites/nextlab-zoom-fellows/` — the
root `index.html` just redirects there automatically.

---

## Viewing locally

From the repo root:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser (it'll redirect to the
fellows hub), or go straight to:

```
http://localhost:8000/websites/nextlab-zoom-fellows/
```

No build step, no dependencies — it's plain HTML/CSS/JS.

---

## Deploying

This is deployed as a static site on Vercel. Import the repo, set the
Framework Preset to **Other**, leave the Root Directory as `.`, and deploy.

---

## Project source code

Each fellow's actual project source lives under `apps/` (currently:
Zoom Momentum). These are kept in this repo for reference but aren't part
of the deployed website — the website links out to each project's own
hosted demo instead. See the README inside each app's folder for setup and
architecture details specific to that project.

---

## License

This project is part of the Zoom Fellowship program at Arizona State
University's Next Lab.
