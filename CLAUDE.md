# Southwest Trip Itinerary — Project Notes for Claude Code

## What this is
A single-file, self-contained HTML itinerary for the Dubin family's Southwest road
trip (June 12–18, 2026). The live version is hosted on GitHub Pages and is read on
phones during the trip by Greg and Keren.

The whole site is ONE file: `index.html`. All CSS and SVG graphics are inline — there
are no external assets, no build step, and no dependencies. Keep it that way so it
loads instantly and works offline.

## How to make edits
When Greg asks for a change (e.g. "change Tuesday's hotel", "add a stop", "fix the
checkout time"), edit `index.html` directly. Match the existing structure:
- Each day is a `.day-label` header followed by a `.day` card.
- Bookings use the `.booking` box pattern; flights add the `flight` class.
- Confirmation numbers/PINs go in `<span class="v conf">`.
- Landscapes are hand-built inline `<svg class="scene">` blocks — edit or add to match.

Keep the visual style consistent (Fraunces + Archivo fonts, desert palette in the
`:root` CSS variables). Do not introduce external image URLs or libraries.

## How to publish a change (do this after every edit, unless told otherwise)
This repo auto-deploys to GitHub Pages from the `main` branch. To push an update live:

```
git add -A
git commit -m "Describe the change"
git push
```

The live site updates within ~30–60 seconds. After pushing, tell Greg it's live and
remind him a hard refresh may be needed on his phone.

## Sensitive info note
This file contains real confirmation numbers, door codes, PINs, and host GPS pins.
The GitHub Pages URL is public but unlisted. If Greg ever wants a "clean" public
version, the approach is to keep codes only in a separate private file and strip them
from index.html.
