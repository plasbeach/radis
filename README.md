# radis

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Recommended Browser Setup

- Chromium-based browsers (Chrome, Edge, Brave, etc.):
  - [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
  - [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)
- Firefox:
  - [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
  - [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) to make the TypeScript language service aware of `.vue` types.

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

## Design Tokens

All colors are defined as CSS custom properties in `src/style.css` and available globally.

### Site Palette

| Variable | Value | Usage |
|---|---|---|
| `--color-brown-dark` | `#47311e` | Primary text, borders, buttons |
| `--color-brown-dark-rgb` | `71, 49, 30` | For use in `rgba()` expressions |
| `--color-brown-deep` | `#2e1e11` | Deep shadows |
| `--color-brown-mid` | `#3a2717` | Mid-tone button inset shadows |
| `--color-beige` | `#e5dac5` | Light backgrounds, text on dark |
| `--color-cream` | `#fff8ee` | Card backgrounds |

### Mascot Colors (patradis & geradis)

| Variable | Value | Usage |
|---|---|---|
| `--mascot-body` | `#c22828` | Red radish body |
| `--mascot-body-highlight` | `#d93535` | Body highlight |
| `--mascot-leaf` | `#3d8a2e` | Green leaves |
| `--mascot-leaf-highlight` | `#5aad42` | Leaf highlight |
| `--mascot-root` | `#8c6644` | Root / tail |
| `--mascot-outline` | `#2e1e11` | Character outline |

Usage example:

```css
.my-element {
  color: var(--color-brown-dark);
  background: var(--color-beige);
  border: 2px solid rgba(var(--color-brown-dark-rgb), 0.2);
}
```
