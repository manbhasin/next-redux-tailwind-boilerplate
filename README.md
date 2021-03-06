# NextJS Tailwindcss Redux Boilerplate build with Vite

This is a [NextJs](https://nextjs.org/) boilerplate project to be used with [Tailwindcss](https://tailwindcss.com), [Redux](https://redux.js.org/).

## What is inside?

This project uses many tools like:

- [NextJs](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org)
- [Tailwindcss](https://tailwindcss.com)
- [Redux](https://redux.js.org/)
- [Eslint](https://eslint.org)
- [Prettier](https://prettier.io)

## Getting Started

### Install

Create the project.

```bash
npx degit https://github.com/manbhasin/next-redux-tailwind-boilerplate my-app
```

Access the project directory.

```bash
cd my-app
```

Install dependencies.

```bash
yarn
```

Serve with hot reload at <http://localhost:3000>.

```bash
yarn run dev
```

### Lint

```bash
yarn run lint
```

### Details

- How to use .env variables ?

  - Add env variables to .env file (use .env.[development/production] as per your current environment)

  - Use `NEXT_` prefix to your env variables to let vite compiler know that these variables can be publicly accessed.

  - _This is as per personal choice._ Use a separate env constant file to export the env variables.

```js
const envConfig = {
    BACKEND_URL: process.env.NEXT_REACT_APP_BACKEND_URL!,
};

export default envConfig;
```

- **What if I have my own font files ?**

  - Add font files in public folder. I have created another folder `font-files` in public and copied all the font files into that
  - Use those files in your global css file to override the defaults. See below

```css
@font-face {
    font-family: 'GT Walsheim Pro Regular';
    font-style: regular;
    src: url('/font-files/GT-WALSHEIM-PRO-REGULAR.TTF') format('truetype'), url('/font-files/GTWalsheimProRegular.woff2')
            format('woff2');
    font-display: swap;
}

html {
    font-family: 'GT Walsheim Pro Regular';
}
```
