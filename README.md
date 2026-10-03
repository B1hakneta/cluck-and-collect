# Cluck & Collect

A cozy, single-file chicken clicker. Open `index.html` in a modern browser, or visit the GitHub Pages site. No installation, libraries, external assets, analytics, accounts, backend, or build step.

Pet the hen, buy five kinds of producers, and unlock seven improvements. Three independent starter goals offer one-time rewards. A golden egg appears after 45–75 seconds of visible play, waits until collected (even through reloads), and awards `max(25, floor(EPS × 30), click power × 10)` eggs.

## Saving and timing

- Production accrues while the page remains open, including background-tab time. There are no closed-page earnings.
- Golden-egg countdowns advance only while the page is visible. Collecting starts the next countdown.
- Version 2 saves use the original `cluck_clicker_save` localStorage key. Valid legacy balances, producer counts, and upgrade purchases migrate on the same origin. New click and golden-egg counters start at zero; existing producers count toward the ownership goal.
- Autosaves every five seconds, after purchases and rewards, and when hiding or leaving the page. Storage errors appear in the footer; gameplay continues. An unreadable or unsupported save is not overwritten automatically. “Start a new farm” confirms a reset and retries saving.
- Browser storage belongs to the site's origin. Progress from a local HTML file does not automatically transfer to GitHub Pages. Import/export is not included.

## Controls and accessibility

Use pointer, touch, or Tab and Enter/Space. All actions are native buttons with visible focus. Unavailable shop buttons remain focusable and explain their requirements. Reduced-motion preferences and browser zoom are supported. The desktop layout places the pasture between the two shops. Panels reflow when needed for browser zoom.

## Publishing

GitHub Pages: deploy from the `main` branch, `/ (root)`. The root contains `index.html`, this README, and an empty `.nojekyll`. See [GitHub Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

