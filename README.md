Use ImgJust to create a wall of images on your website.
It's based on the LaTex paragraph justifying algorithm.
Images are scaled while maintaing their aspect ratios.
The source code is simple: it fits on 2 pages and uses
VanillaJS, so you don't have to worry about dependencies,
efficiency, or page load times.

## Algorithm

Given an ideal height, images are carefully put in rows
so that the width of each row is as close to the width of their
container as possible. Then the rows are scaled to fit their
container perfectly.

## Usage

Include the source code in your web page:
```html
<script src="path/to/imgjust.js"></script>
```

Once the page has loaded, use the ImgJust constructor,
passing in the container for the wall, an array
of HTMLImage objects, and an optional options object:
```js
addEventListener("load", _ => {
  const container = document.querySelector(".imgjust");
  const imgs = document.querySelectorAll(".imgjust img");
  const options = {
    idealHeight: 150,
  }
  const imgjust = new ImgJust(container, imgs, options);
}
```

## Options & Defaults

idealHeight: 150
maxRowImgs = 16
rowGap = 0
columnGap = 0
paddingLeft = 0
paddingRight = 0
paddingTop = 0
paddingBottom = 0

## ImgJust Public Methods
constructor(container, imgs=[], options={})
reload()
addImages(imgs)

## Styling
