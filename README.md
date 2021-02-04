# Sapper Template with Rollup and TailwindCSS
While wiating for SvelteKit I found this to be the easiest way imho to integrate TailwindCSS with Sapper.
**Note:** running `yarn dev` takes a while to complete and this method might not be best suited for massive projects.

## Getting started
Install dependacies `yarn add -D tailwindcss postcss autoprefixer svelte-preprocess postcss-load-config`

## Create configuration files
### PostCSS
Create `postcss.config.js` file in root directory
```js
module.exports = {
    plugins: {
        tailwindcss: {},
        autoprefixer: {},
    },
}
```
### TailwindCSS
Run `npm tailwindcss init` from root in terminal.
Update the purge with: `purge: ['./src/**/*.svelte']`
### Rollup
In the `rollip.config.js` dd the import for `import sveltePreprocess from 'svelte-preprocess';` under the svelte import.
Then under the `client` in `plugins` -> `svelte({...})` add the preprocess:
```js
svelte({
    preprocess: sveltePreprocess({ 
        typescript: true,
        postcss: true 
    }),
    ...
}),
```
Then under the `server` in `plugins` -> `svelte({...})` add the preprocess:
```js
svelte({
    preprocess: sveltePreprocess({ 
        typescript: true,
        postcss: true 
    }),
    ...
}),
```
## Global Styles and TailwindCSS Components
Replace the `<style>` tag in the `/routes/_layout.svelte` file with:
```html
<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
/* Add other global styles below */
</style>
```