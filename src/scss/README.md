## Astro.config.mjsに記載する

```scss
// @ts-check
import { defineConfig } from "astro/config";

// https://astro.build/config
export default defineConfig({
	vite: {
		css: {
			preprocessorOptions: {
				scss: {
					additionalData: `
               @use "src/scss/global/_base.scss" as *;
               @use "src/scss/global/_breakpoint.scss" as *;
               @use "src/scss/global/_color.scss" as *;
               @use "src/scss/global/_font-family.scss" as *;
               @use "src/scss/global/_function.scss" as *;
               @use "src/scss/global/_reset.scss" as *;
          `,
				},
			},
		},

	},
});
```