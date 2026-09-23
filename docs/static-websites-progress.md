# Static Website Context And Progress

Last updated: 2026-05-08

This repo now contains two standalone static websites intended for separate Vercel deployments. They are independent of the Zoom Apps SDK product code in `client/` and `server/`.

## Deployment Roots

| Vercel project | Repo root directory | Purpose |
|---|---|---|
| `nextlab-zoom-fellows` | `nextlab-zoom-fellows/` | Evergreen ASU Next Lab Zoom Fellows hub |
| `zoom-momentum` | `zoom-momentum/` | Public product page for the Zoom Momentum fellowship project |

Each directory is self-contained static HTML/CSS/JS and can be used directly as a Vercel project root. No React build step is required for either site.

## Main Fellows Hub

Directory: `nextlab-zoom-fellows/`

Current direction:

- Uses Zoom-forward branding with a polished ASU/innovation tone.
- Presents the fellowship as an evergreen program and project hub, not an event microsite.
- Groups Liam Wirth and Neha Kashyap as current/continuing fellows.
- Spotlights Advikaa Kapil, Shitij Mathur, and Yash Sawant as newer fellows.
- Links Advikaa's project to `https://zoom-ai-showcase.vercel.app/`.
- Links Shitij's project to the `zoom-momentum` deployment.
- Keeps Yash's project details intentionally omitted until confirmed.

Recent cleanup:

- Removed redundant credibility/partnership content.
- Tightened copy that sounded generic or awkward.
- Improved spacing, top navigation tone, and overall page polish.

## Zoom Momentum Product Page

Directory: `zoom-momentum/`

Current direction:

- Static public-facing marketing page for Zoom Momentum.
- Keeps the bold cobalt/yellow/editorial identity from the original product page.
- Product-first positioning: a Zoom-native side panel for live college lectures.
- Includes sections for demo placeholder, product features, fellowship context, and prototype CTA.
- Mentions Shitij compactly as the student builder through the fellowship context, not as an entrepreneur-style profile.

Implemented UI improvements:

- Refined section heading typography so the hero keeps the serif wordmark while body sections use a cleaner sans display style.
- Reduced hero side-panel mockup opacity and visual competition.
- Tightened demo section spacing and video placeholder hierarchy.
- Replaced weak placeholder CTA language with `Jump to demo`.
- Reduced repeated heavy glass-card styling in lower sections.
- Fixed mobile navigation wrapping by keeping the nav in one compact horizontal row.
- Added custom hash-anchor scrolling so `#demo` lands on the demo section instead of the bottom of the hero mockup.
- Tightened mobile hero sizing and text wrapping to avoid horizontal clipping.

Current placeholder:

- The demo section intentionally reserves space for a future product walkthrough video. Replace the placeholder content once the recording is ready.

## Verification Performed

- Served locally from the repo root with a plain static server on port `4173`.
- Confirmed `http://127.0.0.1:4173/zoom-momentum/` returns `200`.
- Ran `node --check zoom-momentum/script.js`.
- Searched for removed/undesired wording in shipped site content.
- Browser-checked the Zoom Momentum page at mobile and desktop widths.
- Specifically verified mobile hero/nav layout and the mobile `#demo` anchor behavior.

## Notes For Future Work

- Keep both sites dependency-free unless there is a strong reason to add a build step.
- If Vercel caches static CSS/JS aggressively after deployment, add query-versioned asset URLs or configure cache headers.
- When Yash's project details are confirmed, update only the fellow card/profile copy and outbound link.
- When the Zoom Momentum demo video is ready, replace the placeholder with an actual hosted video embed or local optimized asset.
