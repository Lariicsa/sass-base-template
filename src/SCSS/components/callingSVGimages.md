<h1 align="center">
  Using SVG images from a mixing
</h1>

In [📄mixins.scss file](src/SCSS/shared/_mixins.scss) you can find the mixin called _icon_, here I included 3 SVG images in URI format.

So, in the first condition we can see this:

```css
@mixin icon($name, $color) {
  text-indent: -9000px;
  background-repeat: no-repeat;
  $string: #{$color};
  $varcolor: str-replace($string, "#", "%23");

  @if ($name == "ld") {
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 64 64' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M54.625 0H9.375C4.20605 0 0 4.20605 0 9.375V54.625C0 59.7939 4.20605 64 9.375 64H54.625C59.7939 64 64 59.7939 64 54.625V9.375C64 4.20605 59.7939 0 54.625 0ZM22.625 50.75H15.125V24.5H22.625V50.75ZM22.625 20.75H15.125V13.25H22.625V20.75ZM48.875 50.75H41.375V35.75C41.375 33.6826 39.6924 32 37.625 32C35.5576 32 33.875 33.6826 33.875 35.75V50.75H26.375V24.5H33.875V25.9136C35.8398 25.3027 37.1162 24.5 39.5 24.5C44.5864 24.5054 48.875 29.0684 48.875 34.4609V50.75Z' fill='"+$varcolor+"'/%3E%3C/svg%3E%0A");
  }
  .
  .
  .
```

And from the [📄footer.scss](src/SCSS/components/footer.scss) file it's called in this way:

```css
a {
  display: block;
  height: 100%;
  &.ld {
    @include icon("ld", white);
    &:hover {
      @include icon("ld", $grad-bg-solid);
      background-color: linear-gradient(
        0deg,
        rgba(255, 107, 107, 0.5) 40%,
        rgba(224, 41, 98, 0.4) 100%
      );
      cursor: pointer;
    }
  }
}
```

It is necessary to pass the parameters _name of image_ and _color_

Then, [in our example](https://lariicsa.github.io/sass-base-template/) we can visualize the social media images, in this specific case: the _linkedin_ image.
