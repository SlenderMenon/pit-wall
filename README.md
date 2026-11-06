# Pit Wall

A racing strategy game. You're on the pit wall for car 27: pick tyres, time your stops, manage pace, and gamble on safety cars.

## What's new in V2

- **Live track map**: every car moves round the circuit in real time. Pitting cars drop into the pit lane, and the field bunches up behind the safety car.
- **Slower, smarter pacing**: 1× is now about 2.5 s a lap. The game slows down automatically for key moments (safety car, a rival pitting near you, worn tyres, the last 5 laps).
- **Safety car you can't miss**: a striped banner, a flashing yellow screen edge, a vibration on Android, and a "Box or stay out?" decision prompt.
- **Race control alerts**: banners for tyres going off, 5 laps to go, last lap and green flag.

## What's in V1

- **Daily race**: everyone gets the same track, rival strategies and safety car on a given day. Your first run of the day is your official result.
- **Free practice**: random races on any of the four tracks.
- **Four fictional tracks** with different lap counts, pit loss, tyre wear and overtaking difficulty.
- **Share result**: a short text card (position, stints, best lap) that opens your phone's share sheet or copies to the clipboard.
- **Installable app (PWA)**: add it to your home screen and it opens full screen and works offline.

## Files

| File | What it does |
| --- | --- |
| `index.html` | The whole game: layout, styles and logic |
| `manifest.webmanifest` | Tells phones the app's name, colours and icons |
| `sw.js` | Service worker: caches the game so it loads fast and works offline |
| `icons/` | App icons for home screens and browser tabs |

## Run it locally

Double-click `index.html`. The game plays fully. Install and offline mode only switch on once it's served from a real web address (see below).


## Updating

- Changes to `index.html` show up for players next time they open the game online.
- If you change any other file (icons, manifest), bump `CACHE` in `sw.js` (for example `pitwall-v3`) so installed copies pick it up.
