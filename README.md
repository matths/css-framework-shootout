## Materialize

```bash
npm create vite@latest materialize-css -- --template vanilla
cd materialize-css
npm install --save-dev sass
npm install materialize-css@next --save-dev
rm style.css
touch style.scss
echo "import './style.scss'" > main.js
```

## Tailwind

Setup is described here: https://tailwindcss.com/docs/guides/vite

```bash
npm create vite@latest tailwind-css -- --template vanilla
cd tailwind-css
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

