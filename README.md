# IG Carousel Splitter

Split a panoramic image into 1080×1440 (3:4) slides for a seamless Instagram carousel — with zero quality loss.

**Live:** https://mickosis.github.io/ig-carousel/

## Usage

1. Open `index.html` in a browser (or use the live link above). No install, no server.
2. Drop in an image, or click to choose one.
3. Check the dashed cut lines to make sure nothing important sits on a seam.
4. Click **Download .zip** to get every slide in one file, or save slides individually.

Slides are saved as `<name>_01.png`, `<name>_02.png`, … in upload order.

## Size rule

The source image must be **exactly 1440px tall** and **a multiple of 1080px wide**:

| Slides | Source size |
| --- | --- |
| 2 | 2160 × 1440 |
| 3 | 3240 × 1440 |
| 4 | 4320 × 1440 |
| 5 | 5400 × 1440 |
| 6 | 6480 × 1440 |

Anything else is rejected rather than resized, so output is never upscaled or cropped unexpectedly.

## Why there's no quality loss

Each slide is a 1:1 pixel copy of its region of the source — no scaling, no smoothing — encoded as lossless PNG. Everything runs locally in the browser; the image never leaves your machine.

## Notes

- **Download .zip** bundles every slide into `<name>_slides.zip`. On iPhone it saves to the Files app.
- The page loads the Archivo font from Google Fonts; everything else, including the zip, is built locally.

## License

[MIT](LICENSE)
