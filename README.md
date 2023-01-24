# CSS Framework shootout

This is just a quick and dirty attempt to code one and the "same" example with different CSS frameworks.
The goal is not to have pixel perfect matches in every framework, but to compare what it takes to get started with these frameworks, what you need to write to get a similar result, sometimes with the look and feel of the specific framework.

For now it is a top navigation, a logo (not repsonsive, yet) and a full height container with three cards that take use of at least one breakpoint as a responsive example.

## How to compare

To compare markup open the whole Repository code in Visual Studio Code editor.

And to run the examples follow these basic steps:

```bash
cd [css-framework-name]
npm run dev
[meta+click URL provided to open in browser]
```

## Original Vanilla JS Vite Setup for different CSS Frameworks

### Materialize 1.0

```bash
npm create vite@latest materialize-css -- --template vanilla
cd materialize-css
npm install --save-dev sass
npm install materialize-css@next --save-dev
rm style.css
touch style.scss
echo "import './style.scss'" > main.js
```

### Tailwind 3.2

Setup is described here: https://tailwindcss.com/docs/guides/vite

```bash
npm create vite@latest tailwind-css -- --template vanilla
cd tailwind-css
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Bootstrap 5

Setup is similar but different to description here: https://getbootstrap.com/docs/5.3/getting-started/vite/

```bash
npm create vite@latest bootstrap -- --template vanilla
cd bootstrap
npm i --save bootstrap @popperjs/core
npm i --save-dev sass
rm style.css
touch style.scss
```

content of style.scss

```scss
@import "node_modules/bootstrap/scss/bootstrap";
```

content of main.js

```js
// Import our custom CSS
import 'style.scss'

// Import all of Bootstrap's JS
import * as bootstrap from 'bootstrap'
```
