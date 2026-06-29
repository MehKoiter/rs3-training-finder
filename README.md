# RS3 Training Spot Finder

A lightweight single-file web app for finding RuneScape 3 training spots. Filter and sort monsters by combat level, style weakness, slayer requirement, members status, and more.

**[Live demo →](https://mehkoiter.github.io/rs3-training-finder)**

---

## Features

- Filter by combat level range, combat style weakness (melee/ranged/magic), members/F2P status, slayer level, and name
- Sort results by combat level, XP per kill, life points, or name
- **Suggest level range** button — sets min/max enemy level based on your combat level
- **Shareable URLs** — every search updates the URL with your filters; paste the link and the search restores exactly
- Settings persist in localStorage so your last filters are restored on your next visit
- Searches run on page load if settings exist; press Enter anywhere to re-run
- Every result links to the monster's RS3 wiki page; locations link to the wiki too
- RS3-themed dark gold UI with Cinzel serif headings
- No backend, no dependencies, no build step — a single HTML file

## Usage

Enter your combat stats, choose filters, and hit **Find Training Spots** (or press Enter). Results show combat level, life points, XP per kill, weakness, location, aggression, poison status, and any Slayer requirement.

**Style filter** — "Melee" shows monsters weak to slash/stab/crush; "Ranged" shows those weak to arrows or bolts; "Magic" shows those weak to elemental spells.

**Slayer filter** — defaults to 99 (all monsters visible). Lower it to hide monsters whose Slayer requirement exceeds your level.

**Sort** — switch between combat level ↑, XP/kill ↓, life points ↓, or name A–Z. The results header updates to reflect the active sort.

**Shareable URL** — after a search the URL updates automatically. Copy it from the address bar or use the **Copy link** button that appears in the status bar.

## How it works

The app uses an embedded dataset of 68 common RS3 training monsters covering F2P and members content from combat level 1 to 333. All filtering and sorting happen client-side with no API calls.

XP per kill values are approximate (roughly 40% of life points, representing the primary combat stat per kill).

## Hosting

Drop `index.html` anywhere that serves static files:

- **GitHub Pages** — enable Pages in the repo Settings under Pages → Source
- **Netlify** — drag and drop the file at [netlify.com](https://netlify.com)
- **Vercel** — import the repo or drop the file

## Credits

Monster data derived from [runescape.wiki](https://runescape.wiki). Not affiliated with Jagex.
