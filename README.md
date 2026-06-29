# rs3-training-finde
A lightweight web app that queries the RS3 Wiki live to find monsters suited to your combat level and training style. Filter by melee, ranged, or magic weakness, membership status, and enemy combat level range.

# RS3 Training Spot Finder

A lightweight web app that queries the RS3 Wiki live to find monsters suited to your combat level and training style. Filter by melee, ranged, or magic weakness, membership status, and enemy combat level range.

**[Live demo →](https://yourusername.github.io/rs3-training-finder)**

---

## Features

- Live data pulled directly from the [RS3 Wiki](https://runescape.wiki) Cargo API — always up to date
- Filter monsters by combat level range, combat style weakness, and members/F2P status
- Shows combat level, HP, XP per kill, weakness, location, aggression, poison, and Slayer requirements
- Every result links to the monster's full wiki page
- Dark mode support
- No backend, no dependencies, no build step — a single HTML file

## Usage

Enter your combat stats, choose your preferred combat style and any filters, then hit **Search the wiki**. Results are sorted by enemy combat level ascending.

The style filter works by matching against the monster's weakness — selecting "Melee" will show monsters weak to slash, stab, or crush attacks.

## How it works

The app queries the `Monsters` Cargo table on the RS3 Wiki's MediaWiki API:

```
https://runescape.wiki/api.php?action=cargoquery&tables=Monsters&...
```

The wiki supports CORS, so the query runs directly from the browser with no backend required. Up to 500 monsters are fetched per search, deduplicated by name, and filtered client-side by weakness type.

## Hosting

This is a single `index.html` file — host it anywhere that serves static files:

- **GitHub Pages** — upload to a repo and enable Pages in Settings
- **Netlify** — drag and drop the file at [netlify.com](https://netlify.com)
- **Vercel** — import the repo or drop the file

## Credits

Monster data sourced from [runescape.wiki](https://runescape.wiki) under [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/).

Not affiliated with Jagex.
