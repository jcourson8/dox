Title: Macaron - SolidDocs

URL Source: https://docs.solidjs.com/guides/styling-components/macaron

Markdown Content:
[Macaron](https://macaron.js.org/) is compile-time CSS-in-JS library that offers type safety.

* * *

1.  Install and set up the macaron plugin for your bundler:

2.  Within your `vite.config.js` folder, add the macaron plugin prior to other plugins:

```
import { macaronVitePlugin } from "@macaron-css/vite";import { defineConfig } from "vite";export default defineConfig({  plugins: [    macaronVitePlugin(),    // other plugins  ],});
```

* * *

1.  Import `styled` from `@macaron-css/solid` and create a styled component:

```
import { styled } from "@macaron-css/solid";const Button = styled("button", {});
```

2.  Add styles that will be applied to the components by default:

```
import { styled } from "@macaron-css/solid";const Button = styled("button", {  base: {    backgroundColor: "red",    borderRadius: "10px",  },});
```

Variants can be added using the `variants` key:

```
import { styled } from "@macaron-css/solid";const Button = styled("button", {  base: {    backgroundColor: "red",    borderRadius: "10px",  },  variants: {    color: {      violet: {        backgroundColor: "violet",      },      gray: {        backgroundColor: "gray",      },    },  },});
```

Additionally, the `defaultVariants` feature is set to `variants` by default. This can be overridden at the time of usage:

```
import { styled } from "@macaron-css/solid";const Button = styled("button", {  base: {    backgroundColor: "red",    borderRadius: "10px",  },  variants: {    color: {      violet: {        backgroundColor: "violet",      },      gray: {        backgroundColor: "gray",      },    },  },  defaultVariants: {    color: "blue",  },});
```

These components can be used like any other Solid component, with type-safe props derived from your variants. For more information on how to use macaron, visit their [documentation](https://macaron.js.org/docs/installation/).
