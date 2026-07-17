# fucad.github.io

Landing site for **FUCAD ARCADE** — open-source, ad-free, free-forever casual games.

A single static `index.html` with no build step and no dependencies, served by GitHub Pages.
Ported from the `FUCAD Site.dc.html` Claude Design source.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Editing content

The game grid and manifesto principles are data-driven — edit the `GAMES` and `PRINCIPLES`
arrays in the inline `<script>` at the bottom of `index.html`.

Each game entry takes a `github`, `play`, and `app` URL. While one is left as `'#'`, that
store button renders dimmed and non-clickable; fill in a real URL to activate it.

## Routing

Pages are hash-routed: `#home`, `#story`, `#manifesto`. `#games` is a scroll target on the
home page rather than a page of its own.
