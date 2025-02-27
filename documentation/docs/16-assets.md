---
title: Asset handling
---

### Hashing

To include hashes in your asset file names and cache them, you can have Vite process your assets by importing them as shown below:

```html
<script>
	import logo from '$lib/assets/logo.png';
</script>

<img alt="The project logo" src={logo} />
```

If you prefer to reference assets directly in the markup, you can use a preprocessor such as [svelte-preprocess-import-assets](https://github.com/bluwy/svelte-preprocess-import-assets) or [svelte-image](https://github.com/matyunya/svelte-image).

For assets included via `url()` in you may find the [`experimental.useVitePreprocess`](https://github.com/sveltejs/vite-plugin-svelte/blob/main/docs/config.md#usevitepreprocess) option useful:

```js
// svelte.config.js
export default {
	experimental: {
		useVitePreprocess: true
	}
};
```

### Optimization

You may wish to utilize compressed image formats such as `.webp` or `.avif` or responsive images that serve a different size based on your device's screen. For images that are included statically in your project you may use a preprocessor like [svelte-image](https://github.com/matyunya/svelte-image) or a Vite plugin such as [vite-imagetools](https://github.com/JonasKruckenberg/imagetools).
