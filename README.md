# fucad.github.io

The website for **FUCAD ARCADE** — open-source, ad-free, free-forever casual games.
Live at [fucad.github.io](https://fucad.github.io).

## What FUCAD is

FUCAD is a project to make simple arcade and puzzle games a public good rather than a product.
Every game is free, open-source, and ships without ads, paywalls, or data harvesting. Now that
AI can build a polished casual game in a week, these games exist to set a baseline for what
simple entertainment should cost you: nothing, including your attention.

This repo is only the site — the landing page that introduces the project, lists the games, and
carries the manifesto. Each game lives in its own repo under [@fucad](https://github.com/fucad).

## What's on the site

- **Home** — the pitch, plus the arcade grid linking each game to its GitHub repo and app stores.
- **My Story** — why the project exists.
- **Manifesto** — the six principles, and the rules for what qualifies as a FUCAD game.

## The site itself

A single static `index.html`: no build step, no dependencies, no framework, served by GitHub Pages.
Pages are hash-routed (`#home`, `#story`, `#manifesto`); `#games` is a scroll target on the home
page rather than a page of its own.

Local preview:

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Editing content

The game grid and manifesto principles are data-driven — edit the `GAMES` and `PRINCIPLES` arrays
in the inline `<script>` at the bottom of `index.html`.

Each game entry takes a `github`, `play`, and `app` URL. While one is left as `'#'`, that store
button renders dimmed and non-clickable; fill in a real URL to activate it.

## License

Code: MIT · Assets: CC BY
