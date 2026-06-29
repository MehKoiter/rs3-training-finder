# RS3 Training Spot Finder

A lightweight single-file web app for finding RuneScape 3 training spots. Filter monsters by combat level range, combat style weakness, and members/F2P status.

**[Live demo →](https://mehkoiter.github.io/rs3-training-finder)**

---

## Features

- Filter monsters by combat level range, combat style weakness (melee/ranged/magic), and members/F2P status
- Shows combat level, life points, XP per kill, weakness, location, aggression, poison, and Slayer requirements
- Every result links to the monster's full wiki page
- RS3-themed dark gold UI with Cinzel serif headings
- No backend, no dependencies, no build step — a single HTML file

## Usage

Enter your combat stats, choose your preferred combat style and any filters, then hit **Find Training Spots**. Results are sorted by enemy combat level ascending.

The style filter matches against each monster's weakness — selecting "Melee" shows monsters weak to slash, stab, or crush; "Ranged" shows those weak to arrows or bolts; "Magic" shows those weak to elemental spells.

## How it works

The app uses an embedded dataset of 68 common RS3 training monsters covering F2P and members content from combat level 1 to 333. All filtering happens client-side with no API calls.

XP per kill values are approximate (roughly 40% of life points, representing the primary combat stat per kill).

## Hosting

Drop `index.html` anywhere that serves static files:

- **GitHub Pages** — enable Pages in the repo Settings under Pages → Source
- **Netlify** — drag and drop the file at [netlify.com](https://netlify.com)
- **Vercel** — import the repo or drop the file

## Credits

Monster data derived from [runescape.wiki](https://runescape.wiki). Not affiliated with Jagex.
