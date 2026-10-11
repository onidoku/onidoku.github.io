# onidoku.github.io

the website for [onidoku](https://github.com/onidoku/app), live at **https://onidoku.github.io**.

plain HTML and CSS, no build step. every push to `main` publishes it through `.github/workflows/pages.yml`
(one-time setup: **Settings → Pages → Source: GitHub Actions**).

## preview

```sh
python3 -m http.server 8000
```

then open http://localhost:8000. opening `index.html` as a file won't load the fonts.

## screenshots

the images in `img/` are real screenshots of the extension, taken by a script in the main repo. with both repos
checked out side by side (`onidoku/` and `onidoku.github.io/`), run this in `onidoku/`:

```sh
pnpm --filter @onidoku/extension shots
```

it writes the WebP screenshots and the social preview `og.png` here. set `ONIDOKU_SITE=/path/to/this/repo` if it
lives somewhere else.

## credits and licenses

- site code: [FSL-1.1-MIT](LICENSE), like onidoku.
- screenshots show [Pepper&Carrot](https://www.peppercarrot.com) by David Revoy
  ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)) and public-domain books from
  [Standard Ebooks](https://standardebooks.org).
- fonts: [Bricolage Grotesque](https://github.com/ateliertriay/bricolage) and a two-glyph subset of
  [Noto Serif JP](https://fonts.google.com/noto/specimen/Noto+Serif+JP), both under the SIL Open Font License
  (`fonts/OFL-*.txt`).
