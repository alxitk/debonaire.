# Debonaire

Website markup built on the [FLS (Gulp + Webpack)](https://github.com/DenishaMorgan/fls-start) starter template.

## Stack

- Gulp — fonts processing, HTML includes, images, sprites, deployment
- Webpack 5 + webpack-dev-server — JS/SCSS bundling and dev server with hot reload
- SCSS, Pug/HTML includes
- Swiper, SimpleBar, Inputmask, LightGallery, NoUiSlider, Tippy.js, etc.

## Requirements

- Node.js
- npm

## Install

```bash
npm run start
```

Runs `npm i --legacy-peer-deps` (needed because some Gulp plugins have outdated peer dependencies).

## Development

```bash
npm run dev
```

Runs Gulp tasks (fonts/HTML includes) and starts `webpack serve`, opening the project at:

```
http://localhost:8080
```

Changes in `src/` are picked up automatically (HMR).

## Build

```bash
npm run build       # production build (converts images to WebP)
npm run devbuild     # production build without WebP
```

Output goes to the `dist/` folder.

## Other commands

| Command | Purpose |
|---|---|
| `npm run sprite` | build an SVG sprite |
| `npm run fonts` | generate `@font-face` rules from font files (`--rewrite` flag) |
| `npm run deploy` | build + upload via FTP (`gulp deployFTP`) |
| `npm run zip` | build + pack into an archive (`gulp deployZIP`) |
| `npm run bem` | generate a BEM tree from HTML (`fls-bemtree-from-html`) |

## Structure

```
config/               Gulp tasks and Webpack settings (dev/prod)
src/
  html/                HTML includes (header, footer, popups, etc.)
  scss/                styles (base/, fonts/, libs/, style.scss)
  js/                  scripts (files/, libs/)
  img/                 images by section
  components/          standalone components (e.g. sendmail)
  index.html           main page
dist/                  build output (generated, not tracked by git)
```

## Deployment

FTP credentials and the archive path are configured in `config/gulp-settings.js`.
# debonaire.
