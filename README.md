# Vite + Svelte + TypeScript + Tailwind

## Create project

```
mkdir SvelteTemplate
cd .\SvelteTemplate\
npm create vite@latest
```

## Enter name

```
svelte-template
```

## Select

```
Svelte
TypeScript
```

## Open project in vs code:

```
cd .\svelte-template\
code -r .
```

## Update Svelte to version 5

```
npm install svelte@next
```

## Install TypeScript

```
npm install --save-dev @tsconfig/svelte typescript svelte-preprocess svelte-check
```

## Update "tsconfig.node.json" file:

```
"noEmit": false
```

## Update "package.json" file:

```
"devDependencies": {
    "@sveltejs/vite-plugin-svelte": "^4.0.0-next.6",
}
```

## Update "main.ts" file:

```
import "./app.css";
import App from "./App.svelte";
import { mount } from "svelte";

const app = mount(App, { target: document.getElementById("app")! });

export default app;
```

## Install Tailwind

```
https://tailwindcss.com/docs/guides/vite
https://tailwindcss.com/docs/guides/sveltekit
```

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## Update "tailwind.config.js" file:

```
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{html,js,svelte,ts}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

## Update "app.css" file:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Add tailwind classes to "App.svelte" file:

```html
<h1 class="text-3xl font-bold underline">Hello world!</h1>
```

## Remove other css styles

## Install and run the app

```
npm i
npm run dev
```
