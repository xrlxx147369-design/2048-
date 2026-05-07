# GitHub Pages Publishing Design

## Goal

Make the 2068 static game accessible outside the local network through GitHub Pages.

## Approach

Keep the project as a static site. GitHub Pages can publish `index.html` and `2068-kids.html` directly from the repository root, so no backend or multiplayer relay is needed for this sharing use case.

## Files

- `index.html`: Entry page with GitHub Pages sharing copy and current-page link copying.
- `2068-kids.html`: Game page, unchanged.
- `.nojekyll`: Tells GitHub Pages to serve files as plain static assets without Jekyll processing.

## Data Flow

Visitors open the GitHub Pages URL, land on `index.html`, then click the relative link to `2068-kids.html`. The share input uses `window.location.href`, so it automatically shows the live public URL after deployment.

## Notes

This supports public access to the game page. It does not add real-time multiplayer synchronization.
