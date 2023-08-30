# Astro 3 Optimized Images Template

## This is Work in Progress, use with caution

## Set Up

1. Copy `.env.example` to `.env`.
2. Adjust widths in `.env` to your liking. Defaults are 100, 300, 900 and 1800 pixels. 
3. Use in pages like:

```js
---
import { Image, getImage } from "astro:assets";
import Layout from "../../layouts/default.astro";
import OptImage from "../../components/OptImage.astro"
import img1 from "./reepolee-labs.jpg";

---
<Layout title="About Page">
	<div class="flex justify-center">
	<OptImage 
		src={img1} 
		sizes="(max-width: 320px) 100px, (max-width: 640px) 300px, (max-width: 1000px) 800px, 100vw" 
		alt="Reepolee Labs" 
		class="rounded-2xl" 
	>
	</div>
</Layout>

```

## What it does

Images get generated in predefined widths from `.env` in `webp` and `avif` formats. Fallback is the original image. We set up a `srcset` for every image but you're in full control of your sizes on different pages, just adjust the prop.
