# Astro Optimized Image

# Set Up

1. Copy `.env.example` to `.env`.
2. Adjust widths in `.env` to your liking. Defaults are 100, 300, 900, 1800 pixels. 
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
