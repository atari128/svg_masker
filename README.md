# SVG Masker

<<<<<<< HEAD
=======
## TLDR

![Demo image](demo.jpg)

Use a black and white jpeg image as a mask for another jpeg and save it as SVG


>>>>>>> 3cab7006452fe068337a6a920886a39220c3c4ee
## Overview

SVG Masker is a simple, client-side web application that allows you to apply a mask to an image and export the result as a scalable vector graphic (SVG) file. It's a simple way of embedding two jpeg images inside a single SVG as a smaller alternative to a PNG with aplha channel.

## Features

*   **Masked Image Generation:** Combine a main image with a mask image to create a new SVG where transparency is controlled by the mask.
*   **Flexible Masking:** The mask image can have different dimensions than the main image. The application ensures the mask is scaled correctly while preserving its aspect ratio, preventing stretching or distortion.
*   **Luminance Masking:** Utilizes the luminance values of the mask image: black areas will result in full transparency, white areas in full opacity, and shades of gray in partial transparency.
*   **Client-Side Processing:** All image processing and SVG generation happen directly in your browser, ensuring privacy and no server-side overhead.
*   **Configurable Output Size:** Choose whether the generated SVG should adopt `100%` width and height (responsive) or retain the exact pixel dimensions of the input image.
*   **Scalable Output:** The output SVG is designed with a `viewBox` attribute, ensuring the content scales correctly and maintains its aspect ratio whether you choose responsive (`100%` width/height) or fixed-pixel output.

## How to Use

1.  **Open the Application:** Open the `index.html` file in your web browser (located in the `v2` directory).
2.  **Select Language:** (Optional) Choose your preferred language (English or Eesti) from the dropdown selector in the header.
3.  **Select Main Image:** Click the "Image (JPG)" input field and select your main image file (JPEG format recommended).
4.  **Select Mask Image:** Click the "Mask (JPG)" input field and select your mask image file (JPEG format recommended). For best results, use a black and white image where white areas are opaque and black areas are transparent.
5.  **Configure Output Size:** Check or uncheck the "Make output responsive (100% width/height)" checkbox based on your preference.
6.  **Generate Preview:** Click the "Generate" button. The masked image will appear in the "Preview" area.
7.  **Download SVG:** Once the preview is generated, the "Download" button (below the preview) will become active. Click it to save the `masked_image.svg` file to your computer.

## Technical Details

*   **Single File Application:** The entire application (HTML, CSS, and JavaScript) is contained within a single `index.html` file.
*   **Pure JavaScript:** No external libraries or frameworks are used.
*   **Base64 Embedding:** Images are converted to Base64 data URLs and embedded directly into the SVG to ensure a self-contained, portable, and display-reliable output.

## Development Notes

Updated prettier UI - generated with gemini