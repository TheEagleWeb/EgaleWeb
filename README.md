# create-svelte

Everything you need to build a Svelte project.

## Clone a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# clone project into file
git clone https://github.com/TheEagleWeb/EgaleWeb.git
# open the newly created my-app
cd EgaleWeb
```

## Install Tailwind CSS
Install tailwindcss and its peer dependencies, then generate your `tailwind.config.js` and `postcss.config.js` files:
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
