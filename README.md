# Cluck & Collect

[Play the game](https://b1hakneta.github.io/cluck-and-collect/)

A cozy desktop chicken clicker with an optional, faster third-person escape game. One HTML file, no installation, libraries, external assets, analytics, accounts, backend, or build step.

Grow through **50 farm levels** with five producers and **42 upgrades**: the original seven plus 35 improvements. Three independent starter goals grant one-time rewards. A golden egg appears after 45–75 seconds of visible play, waits until collected (even through reloads), and awards `max(25, floor(EPS × 30), click power × 10)` eggs. Original producer prices, price growth, and the seven original upgrade calculations remain intact.

## Grandma's chase

Grandma wants chicken for supper. Escape across ten encounters in a minimal 3D farmyard, with a perspective camera following behind the hen. **The chicken physically turns around and shoots eggs directly from its rear**, then turns back. There is no separate weapon.

| Control | Action |
| --- | --- |
| WASD | Move relative to the camera |
| Mouse | Manually aim; click the arena to capture the pointer when supported |
| Hold left mouse / Space / F | Turn and fire on a cooldown |
| Shift | Dodge in the movement direction, or backward while standing |
| Q / E or left / right arrows | Rotate the camera for keyboard aiming |
| Up / down arrows | Adjust aim height |
| P | Pause / resume |
| Escape | Release the pointer and pause |

No aim assist or homing: projectiles follow your aim and can miss. Grandma chases, marks an orange circle, winds up, and lunges at that position. Move clear or dodge with brief invulnerability. Hits during her recovery deal double damage. Dodge recharges in 1.3 seconds. Holding fire works; rapid clicking is unnecessary. In browsers without pointer capture, moving the pointer inside the arena still aims.

The first encounter is available immediately; the others unlock at farm levels 5, 10, 15, 20, 25, 30, 35, 40, and 45. Later encounters have more determination, faster pursuit, and shorter windups. Each successful escape awards eggs once; replays are for fun. Getting caught never removes farm earnings or purchases. Escape equipment adds hearts and shot strength, and every ten farm levels adds a point of strength.

Combat pauses when you switch tabs, leave the arena, or the window loses focus. Saved encounters resume only when you choose. The renderer generates every mesh, camera projection, flat color, and animation inside the HTML. No engine, textures, or models are downloaded.

## Saving and timing

- Farm production accrues while the page remains open, including background-tab time. Closed-page time earns nothing.
- Golden-egg countdowns advance only while visible. Collecting starts the next countdown.
- Version 4 saves use the original `cluck_clicker_save` localStorage key. Original, version 2, and version 3 saves migrate on the same origin. Existing balances, purchases, goals, golden eggs, equipment, and completed encounters are preserved. Version 3 turn-based encounters migrate to paused third-person encounters with their remaining hearts and determination.
- Original saves start the new click and golden-egg goal counters at zero; existing producers count toward the ownership goal. Production is always recomputed from validated purchases.
- Autosaves every five seconds, after purchases and rewards, when combat pauses, and when hiding or leaving the page. Storage failures appear in the footer while gameplay continues. An unreadable or unsupported save is not automatically overwritten. “Start a new farm” confirms a complete reset and retries saving.
- Browser saves belong to the site's origin. Progress from a local HTML file does not automatically transfer to GitHub Pages. Import/export is outside this update.

## Accessibility and layout

Designed for desktop keyboard and mouse. Native buttons support Enter/Space, with visible keyboard focus. Shop cards are built once and updated in place; passive counters refresh at most ten times per second. Browser zoom reflows the panels. Reduced motion removes cosmetic spinning, hopping, and floating animations; essential player movement and manual camera aiming remain. Combat is optional and can be paused at any time.

## Publishing

GitHub Pages deploys from `main`, `/ (root)`. Only `index.html`, this README, and an empty `.nojekyll` belong in the repository. See [GitHub Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).
