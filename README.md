<h1 align="center">
  Sass folders and files organization
</h1>

_Just an example/recommendation of how to organize sass files_

[Here you can check out the demo](https://lariicsa.github.io/sass-base-template/)

## Table of Contents

1. [Base Estructure](#Base-Estructure)
2. [📄Index File](#Index-File)
3. [📂Components](src/SCSS/components)
  1. [📄Footer](src/SCSS/components/footer.scss)
     1. [📄Using SVG Images from Mixins](src/SCSS/components/footer.scss)
  2. [📄Header](src/SCSS/components/header.scss)
4. [📂Shared](src/SCSS/shared)
  1. [📄mixins](src/SCSS/shared/_mixins.scss)
  2. [📄variables](src/SCSS/shared/_variables.scss)
  3. [📄global](src/SCSS/shared/global.scss)
  4. [📄normalize](src/SCSS/shared/normalize.scss)


## Base Estructure
    .
    ├── src
      ├── SCSS
        ├── components
          ├── header.scss
          ├── footer.scss
        ├── shared
          ├── _mixins.scss
          ├── _variables.scss
          ├── global.scss
          ├── index.scss
          ├── normalize.scss
       

## Index File

_This file contains general imports of main files_

```css
@import "global/normalize.scss";
@import "global/shared.scss";
@import "components/about.scss";
@import "components/cards.scss";
.
.
.
```
[Check the .index.scss file](src/SCSS/index.scss)
