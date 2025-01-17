# Typography

The Onyx design system relies on a default (sans-serif) and a monospace font family.

Onyx is intended to be used with the following font families which are open-source
and free to use under the [SIL Open Font License](https://en.wikipedia.org/wiki/SIL_Open_Font_License):

- Default: [Source Sans 3](https://fontsource.org/fonts/source-sans-3)
- Monospace: [Source Code Pro](https://fontsource.org/fonts/source-code-pro)

## Using custom font families

::: info Default font families
The above default font families are already bundled into the component library
so you don't need to install them manually.
:::

If you want to use custom font families, you need to install them and override the following CSS variables manually.

We recommend installing font families as npm package using [Fontsource](https://fontsource.org).

::: code-group

```css [custom.css]
/* import your custom fonts here... */
:root {
  --onyx-font-family: "My custom font family", sans-serif;
  --onyx-font-family-mono: "My custom mono font family", monospace;
}
```

```ts [main.ts]
// make sure to import your custom styles AFTER "sit-onyx/style.css"
import "custom.css";
```

:::
