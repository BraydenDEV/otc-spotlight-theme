# otc-spotlight-theme

## Overview

This document outlines the changes made to the product thumbnails on both **desktop** and **mobile** views. The customization includes:

1. **Ensuring that the product images fit within their containers without zooming in.**
2. **Adding a text overlay at the bottom of each thumbnail.**

## CSS Changes

### Desktop

For desktop, the following styles were applied:

```css
.thumbnail-wrapper {
  position: relative;
}
.thumbnail-wrapper img {
  max-width: 100%;
  height: auto;
  object-fit: contain;
}
.thumbnail-overlay-text {
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: #242833;
  color: white;
  padding: 5px 10px;
  width: 100%;
  text-align: center;
}
```

#### Explanation:

- `.thumbnail-wrapper`: Sets the position to **relative** so that the child elements can be positioned absolutely within it.
- `.thumbnail-wrapper img`: Ensures that the image fits within its container without stretching or zooming.
- `.thumbnail-overlay-text`: Positions the text overlay at the bottom of the image and sets its background color and text alignment.

### Mobile

For mobile, the following styles were applied:

```css
@media screen and (max-width: 749px) {
  img {
    object-fit: contain !important;
    max-width: 100% !important;
    height: auto !important;
  }
  .thumbnail-overlay-text {
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: #242833;
    color: white;
    padding: 5px 10px;
    width: 100%;
    text-align: center;
  }
}
```

#### Explanation:

- `img`: Overrides any existing styles to ensure that the image fits within its container.
- `.thumbnail-overlay-text`: Ensures that the text overlay appears the same way on mobile as it does on desktop.

---

By applying these styles, I've ensured that the product thumbnails look **consistent** and **well-designed** across all devices.

---
