# @sit-onyx/figma-utils

## 1.0.0-alpha.0

### Major Changes

- 0211e6e: fix(scss): remove `:root` selector

  When importing Figma variables with format `SCSS`, the resulting `.scss` file will put the variables
  directly in the root of the file instead of nesting them inside a `:root` selector.

  The reason for this is that the variables must be importable / usable into other `.scss` files but nesting
  them inside a selector will make them unusable.

  **old:**

  ```scss
  // variables.scss
  :root {
    $some-variable: 42;
  }
  ```

  **new:**

  ```scss
  // variables.scss
  $some-variable: 42;
  ```

### Minor Changes

- 0211e6e: feat(css): add CLI option `selector`

### Patch Changes

- eebf509: fix(parse): remove mode name if its the default Figma mode name "Mode 1"
