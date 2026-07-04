# F1 2026 season dashboard

A single-file Formula 1 season dashboard: interactive 3D globe with the full 2026
race calendar, session times converted to UAE time (GST, UTC+4), live driver and
constructor standings, race results, and a rolling news ticker.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The dashboard. Content is AES-256 encrypted — a password is required to view. |
| `news.json` | Latest F1 headlines, refreshed automatically by the scheduled workflow. |
| `results.json` | Manual race-results fallback, read by the page when the live API is unavailable. |
| `.github/workflows/f1-news.yml` | Scheduled job that fetches public F1 news feeds and updates `news.json`. |

## Hosting

Served as a static site via GitHub Pages. The page runs entirely in the browser;
standings come from the public Jolpica F1 API at load time.

## Access

The page shows a password prompt. After a successful unlock the browser remembers
the password locally on that device.
