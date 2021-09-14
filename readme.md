# vue-zoom-on-hover

[![last commit](https://img.shields.io/github/last-commit/174n/vue-zoom-on-hover.svg)](https://github.com/174n/vue-zoom-on-hover/commits/master)
[![version](https://img.shields.io/npm/v/vue-zoom-on-hover.svg)](https://www.npmjs.com/package/vue-zoom-on-hover)
![downloads](https://img.shields.io/npm/dm/vue-zoom-on-hover.svg)
![gziped](https://img.badgesize.io/https://unpkg.com/vue-zoom-on-hover@latest/dist/index.esm.min.js?compression=gzip)
[![license](https://img.shields.io/npm/l/vue-zoom-on-hover.svg)](https://github.com/174n/vue-zoom-on-hover/blob/master/license)

Vue.js component that shows the full image or a scaled image in the image area on hover. Forked from [here](https://github.com/Intera/vue-zoom-on-hover)

## Demo
[Live demo](https://174n.github.io/vue-zoom-on-hover/example/)

## Usage
Install package:
```bash
npm i vue-zoom-on-hover
```

Register the component:
```js
import ZoomOnHover from "vue-zoom-on-hover";
Vue.use(ZoomOnHover);
````

With cdn:
```html
<script type="module">
  import ZoomOnHover from "https://unpkg.com/vue-zoom-on-hover@latest/dist/index.esm.min.js";
  Vue.use(ZoomOnHover);
  new Vue({
    el: "#app"
  })
</script>
```

Use it like this:
```html
<div style="width:400px">
  <zoom-on-hover img-normal="image.jpg"></zoom-on-hover>
</div>
```

All options:
```html
<zoom-on-hover img-normal="image.jpg" img-zoom="bigger-image.jpg" :scale="1.5" :disabled="true"
  @loaded="onload" @resized="onresize"></zoom-on-hover>
```

# Features
* enabled/disabled property
* custom scale for zoomed image
* optionally a separate zoom image
* event when all images loaded
* event when images resized (responsive css, etc)

# Caveats
if the parent container is bigger than the source image, the normal image stretches to the size of the parent container but the zoom image will have the original width (will be smaller for example)

# Possible enhancements
* support for touch devices
