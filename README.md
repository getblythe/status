# Status page

The public status page for the app, served by GitHub Pages so it stays up when the app's own hosting doesn't.

It's one static file, `index.html`. Every minute it reads the app's public `/status.json` feed, which carries the notices published from the ops incident screen. If the feed can't be read it says it can't reach the app; it never falls back to "everything is working".

- To point it at another environment, change `FEED_URL` near the bottom of `index.html`.
- During a long outage, edit `index.html` here by hand with a short note.
- Full details: `docs/runbooks/status-page.md` in the app repo.

Fonts: Figtree and Young Serif, under the SIL Open Font License 1.1 (see `assets/FONTS.md`).
