# Open Digital Education React Boilerplate with Vite

This is a [ReactJS](https://reactjs.org) + [Vite](https://vitejs.dev) boilerplate.

## What is inside?

Many tools are already configured like:

- [ReactJS](https://reactjs.org)
- [Vite](https://vitejs.dev)
- [TypeScript](https://www.typescriptlang.org)
- [React i18next](https://react.i18next.com/)
- [Eslint](https://eslint.org)
- [Prettier](https://prettier.io)
- [Husky](https://github.com/typicode/husky)
- [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci)

## Getting Started

### Install

Create the project with the name of your app (Ex: blog)

```bash
npx degit opendigitaleducation/ode-react-boilerplate blog
```

Go to the project directory.

```bash
cd blog
```

Install dependencies.

```bash
yarn
```

Open your project with Vite Server + HMR at <http://localhost:8080>.

```bash
yarn dev
```

## Dev

### [Server Options](https://vitejs.dev/config/server-options.html)

You can change Vite Server by editing `vite.config.ts`

```bash
server: {
  host: "0.0.0.0",
  port: 8080,
  open: true // open the page on <http://localhost:8080> when dev server starts.
}
```

### Absolute Imports

You should use absolute imports in your app

```bash
Replace ../components/* by components/*
```

Edit `vite.config.ts` and add an `alias`

> Telling Vite how to build import path:

```bash
alias: [
  { find: "~", replacement: path.resolve(__dirname, "src") },
  {
    find: "components",
    replacement: path.resolve(__dirname, "./src/components"),
  },
]
```

Add your new path to `tsconfig.json`:

> Telling TypeScript how to resolve import path:

```bash
"baseUrl": "./src",
"paths": {
  "components/*": ["./components/*"],
}
```

### Lint

```bash
yarn lint
```

### Prettier

```bash
yarn prettier:write
yarn prettier:check
```


### Lighthouse

> LHCI will check if your app respect at least 90% of these categories: performance, a11y, Best practices and seo

```bash
yarn lighthouse
```

### Pre-commit

When committing your work, `pre-commit` will start `yarn lint-staged`:

> lint-staged starts lint + prettier

```bash
yarn pre-commit
```

## Build

TypeScript check + Vite Build

```bash
yarn build
```

## Preview

```bash
yarn preview
```

## License

This project is licensed under the AGPL-3.0 license.
