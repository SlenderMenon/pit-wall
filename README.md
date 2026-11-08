# Pit Wall

A racing strategy game. You're on the pit wall for car 27: pick tyres, time your stops, manage pace, and gamble on safety cars.

## What's new in V4

- **Smarter rivals**: each team ranks every 1 and 2 stop plan for the track and picks from the best, covers undercuts, and delays stops when rain is forecast.
- **Varied races**: your grid slot (P4 to P9) and your car's pace change every race. The brief tells you how quick you are today.
- **Balance**: a perfect strategist now wins about a third of the time (it was 73 to 99% in V3). A lazy one-stop almost never wins.
- **Four new circuits**: Yamuna Ring (dusty track that rubbers in), Selatan Tropic Circuit (heat and downpours), Ardenne Forest Circuit (long lap, frequent safety cars, rain on part of the lap) and Eifelring (cold, slow-warming tyres).
- **Weather**: rain forecasts with a probability, a track wetness meter, Inters and Wets, and a "fastest tyre now" hint. Using wet tyres lifts the two-compound rule.
- **Ghost races**: after any race, add your 3-letter tag and tap "Challenge a friend". The link carries the exact race, and your friend races against your ghost car with a head-to-head result at the end.

To tune difficulty, change the `BAL` line near the top of the script in `index.html`.

## What's new in V3

- **Live track map**: every car moves round the circuit in real time. Pitting cars drop into the pit lane, and the field bunches up behind the safety car.
- **Slower, smarter pacing**: 1× is now about 2.5 s a lap. The game slows down automatically for key moments (safety car, a rival pitting near you, worn tyres, the last 5 laps).
- **Safety car you can't miss**: a striped banner, a flashing yellow screen edge, a vibration on Android, and a "Box or stay out?" decision prompt.
- **Race control alerts**: banners for tyres going off, 5 laps to go, last lap and green flag.

## What's in V2

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

## Put it online

1. Create a GitHub repository called `pit-wall` and upload these files (keep the `icons` folder).
2. On Netlify: **Add new site → Import an existing project → GitHub**, pick `pit-wall`, leave the build command empty, publish directory `.`, then deploy.
3. Rename the site under **Site configuration → Change site name**.

Every time you change a file on GitHub, Netlify redeploys automatically within a minute.

## Updating

- Changes to `index.html` show up for players next time they open the game online.
- If you change any other file (icons, manifest), bump `CACHE` in `sw.js` (for example `pitwall-v3`) so installed copies pick it up.
