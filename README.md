<h1 align="center">
  Sass folders and files organization
</h1>

_Just an example/recommendation of how to organize sass files_

## Table of Contents

1. [Base Estructure](#Base-Estructure)
1. [📄Index File](#Index-File)
1. [📂Components](src/SCSS/components)
  - [📄Footer](src/SCSS/components/footer.scss)
  - [📄Header](src/SCSS/components/header.scss)
1. [📂Shared](src/SCSS/shared)
  - [📄mixins](src/SCSS/shared/_mixins.scss)
  - [📄mixins](src/SCSS/shared/_variables.scss)
  - [📄mixins](src/SCSS/shared/global.scss)
  - [📄mixins](src/SCSS/shared/normalize.scss)


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
