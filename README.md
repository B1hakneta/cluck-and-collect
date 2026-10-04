# Cluck & Collect

A cozy, single-file chicken clicker. Open `index.html` in a modern browser, or visit the GitHub Pages site. No installation, libraries, external assets, analytics, accounts, backend, or build step.

Pet the hen, buy five kinds of producers, and grow through **50 farm levels** with **42 upgrades**: the original seven plus 35 new improvements. Three independent starter goals offer one-time rewards. A golden egg appears after 45–75 seconds of visible play, waits until collected (even through reloads), and awards `max(25, floor(EPS × 30), click power × 10)` eggs.

## Grandma's chase

Ten optional encounters take place in a minimal 3D farmyard drawn with a small built-in geometry renderer. Grandma wants chicken for supper. Read her next reach, waddle to safety, then **turn around and shoot an egg directly from the chicken's rear**. The hen turns back afterward. There is no separate weapon.

- The first encounter is available immediately. Further encounters unlock at farm levels 5, 10, 15, 20, 25, 30, 35, 40, and 45.
- Every action is a turn. Amber lanes show where Grandma will reach. Dodging charges a double-strength egg; resting restores a heart. Later encounters have two-handed sweeps, and Grandma pauses every fourth turn.
- Each successful escape awards eggs once. Replays are for fun. Getting caught never removes eggs or farm purchases.
- Escape-kit upgrades add hearts; rear-shot practice adds strength. Every ten farm levels adds one strength too.
- Use the buttons or A / D to waddle, F to turn and shoot, and R to rest while focused inside the encounter. Encounters and their rewards persist through reloads.
- All 3D shapes, camera projection, flat lighting, and animations are generated inside the HTML. No external engine, textures, or models are loaded.

## Saving and timing

- Production accrues while the page remains open, including background-tab time. There are no closed-page earnings.
- Golden-egg countdowns advance only while the page is visible. Collecting starts the next countdown.
- Version 3 saves use the original `cluck_clicker_save` localStorage key. Original saves and version 2 saves migrate on the same origin. Version 2 goal progress and golden eggs remain intact. Original saves begin the new click and golden-egg counters at zero; existing producers count toward the ownership goal. New upgrades, completed encounters, and the current fight are saved too.
- Autosaves every five seconds, after purchases and rewards, and when hiding or leaving the page. Storage errors appear in the footer; gameplay continues. An unreadable or unsupported save is not overwritten automatically. “Start a new farm” confirms a reset and retries saving.
- Browser storage belongs to the site's origin. Progress from a local HTML file does not automatically transfer to GitHub Pages. Import/export is not included.

## Controls and accessibility

Use pointer, touch, or Tab and Enter/Space. All actions are native buttons with visible focus. Unavailable shop buttons remain focusable and explain their requirements. Reduced-motion preferences and browser zoom are supported. The desktop layout places the pasture between the two shops. Panels reflow when needed for browser zoom.

## Publishing

GitHub Pages: deploy from the `main` branch, `/ (root)`. The root contains `index.html`, this README, and an empty `.nojekyll`. See [GitHub Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

