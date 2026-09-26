# istvankis.com

Static splash site (GitHub Pages, custom domain via CNAME, served through Fastly).
Plain HTML/CSS/JS — no build step. Edit the files directly and deploy by pushing to `main`.

## Baseline rules

- **No prompt-related or AI-authored commentary anywhere** — not in HTML, CSS, JS,
  or any other file. Never leave comments that restate the request, the intent, the
  expected behavior, or the reasoning behind a change (e.g. "make this lazy so no
  cookie is set", "self-host fonts to avoid sending IP to Google"). Code and markup
  must stand on their own. Ordinary, self-evident structure is enough; if a comment
  would only narrate what the code already says or why it was asked for, omit it.
  This applies to new code and to anything touched during edits.

## Privacy posture (why the site is the way it is)

- Fonts are self-hosted (`fonts.css` + `fonts/`), so no request reaches Google on load.
- The Cal.com booking widget loads in an `about:blank` iframe whose `src` is set only
  on click — nothing third-party is contacted until the visitor opens it.
- Keep this property: never eagerly load third-party embeds/trackers on page load.
