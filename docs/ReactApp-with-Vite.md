# ReactApp with Vite

## Manual building a web app with Vite

This repo was building by [Vite](https://vitejs.dev/guide/) + [React](https://stackblitz.com/edit/vitejs-vite-5hwepw?file=index.html&terminal=dev).

###  A. Start Vite to render webpage

- Install vite 

```
npm install -D vite
```

- set index.html

src/index.html

```html
<p>Hello Vite!</p>
```

-   project structure

```
/vite-app-js
├── index.html 
├── .gitignore 
├── package-lock.json 
├── package.json 
└── Readme.md
```

- Then run the vite CLI in your terminal:

```
npx vite 
```

###  B. Start Vite to render react

structure

```
/vite-react-js
├── src 
│  ├── components
│  │   └── App.js
│  ├── index.html 
│  └── index.js
├── .gitignore 
├── package.json 
└── Readme.md
```

prepare the initial file: `src/index.html`, `src/index.js`, `src/components/App.js`:

`src/index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Vite ReactApp</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="index.js"></script>
  </body>
</html>
```

-   `src/index.js`

```js
import { createRoot } from "react-dom/client";
import { App } from "./components/App";

const container = document.getElementById("app");
const root = createRoot(container)
root.render(<App />);
```

-   `src/components/App.js`

```js
export function App() {
  return <h1>Hello world!</h1>;
}
```

- install react react-dom

```
npm i --save react react-dom  
```

- Add `"start"` scripts to the `package.json` file  

```
  "scripts": {
    "dev": "vite", // start dev server, aliases: `vite dev`, `vite serve`
    "build": "vite build", // build for production
    "preview": "vite preview" // locally preview production build
  },
```

- run react

```sh
npm dev
```

or

```sh
npx vite src/index.html
```

### `.gitignore`

- `.gitignore`

```shell
/node_modules
/.parcel-cache
/dist
/.pnp
.pnp.js

# testing
/coverage

# production
/build

# misc
.DS_Store
.env.local
.env.development.local
.env.test.local
.env.production.local

npm-debug.log*
yarn-debug.log*
yarn-error.log*
```

## Running this project

This project is set up with [Parcel Bundler](https://parceljs.org/), an npm package
that compiles our frontend assets and comes with an integrated development server.

The dev server runs on port `5173` by default, but will use another if `5173` is
being used by another application.

- Clone the repo.
- Navigate into the project folder.
- Run `npm i` to download the project's dependencies listed in the `package.json`.
- Run `npm dev` to compile the React project and spin up the app on `http://localhost:5173`.
