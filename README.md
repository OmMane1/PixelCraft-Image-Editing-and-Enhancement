# PixelCraft-Model.Image-Editing-and-Enhancement

**PixelCraft** is an image processing application that offers a range of tools for manipulating and
enhancing images. The project is designed to allow users to perform common image editing tasks like
flipping, adjusting brightness, applying filters, splitting and combining RGB components, and much
more. All operations are coded from scratch!

### **Features:**

* Image Loading and Saving: Supports loading and saving of images in PNG, JPEG, and PPM formats.
* Color Component Visualization: Extract and display red, green, and blue components of an image.
* Image Flipping: Perform horizontal and vertical flips on an image.
* Brightness Adjustment: Increase or decrease image brightness with simple adjustments.
* RGB Splitting and Combining: Split images into their RGB components and recombine them.
* Filters: Apply blur, sharpen, and sepia effects to enhance image aesthetics.
* Compression: Compress your image by a specified percentage.
* Histogram: Generate a histogram of the image and analyze the frequency of pixel value distribution.
* Color Correct: Align the peaks of the individual channels to generate a color-corrected image.
* Levels Adjust: Adjust an image's blacks, whites, and mids to generate a level-adjusted image.
* Split preview: Generate a preview image by applying a transformation or filter on a percentage of the image.

### **Image Transformation Examples**

Here are some sample transformations you can achieve with PixelCraft:

<table>
  <thead>
    <tr>
      <th>Original Image</th>
      <th>Transformation</th>
      <th>Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="13" align="center">
        <img src="res/dog.jpg" width="250"/>
      </td>
      <td><b>Horizontal Flip</b></td>
      <td><img src="res/dog-horizontal.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Vertical Flip</b></td>
      <td><img src="res/dog-vertical.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Horizontal + Vertical Flip</b></td>
      <td><img src="res/dog-horizontal-vertical.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Brighten</b></td>
      <td><img src="res/dog-brighten.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Dim</b></td>
      <td><img src="res/dog-dim.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Blur Filter</b></td>
      <td><img src="res/dog-blur.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Sharpen Filter</b></td>
      <td><img src="res/dog-sharpen.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Sepia Filter</b></td>
      <td><img src="res/dog-sepia.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Red Component</b></td>
      <td><img src="res/dog-red-component.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Intensity Component</b></td>
      <td><img src="res/dog-intensity.jpg" width="250"/></td>
    </tr>
    <tr>
      <td><b>Compressed (50%)</b></td>
      <td><img src="res/dog-compressed.png" width="250"/></td>
    </tr>
    <tr>
      <td><b>Split Preview (50% Sepia)</b></td>
      <td><img src="res/dog-spilt.png" width="250"/></td>
    </tr>
  </tbody>
</table>




### **Getting Started:**

* Java 8 or higher
* A compatible image viewer for output files (e.g., Paint)

### **Installation:**

1. Clone the repository from GitHub:

```
   git clone https://github.com/OmMane1/PixelCraft-Image-Editing-and-Enhancement.git
```

2. Double click on the JAR file named -> "PixelCraft - Image Editing and Enhancement.jar"

### **Running the Application:**

Once UI is open, you can load an image for editing. 
This application supports various image manipulations, including loading, saving, color component extraction, flipping, brightening, splitting and combining RGB components, and applying filters like blur, sharpen, and sepia.

### **License:**

This project is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for more details.
You are free to use, modify, and distribute `colors.ppm` file included in this project, provided that credit is given to the authors.


### **Contact:**

For any questions or suggestions, feel free to reach out to the project maintainers:

* Om Mane - mane.om@northeastern.edu
* Sumit Kanu - kanu.s@northeastern.edu

### **Citation:**

* Alatawi, M. (n.d.). Adult brown and white Pembroke Welsh Corgi near the body of water [Photograph].
  Pexels. https://www.pexels.com/photo/adult-brown-and-white-pembroke-welsh-corgi-near-the-body-of-water-14281404/

* Pixabay. (n.d.). Yellow car illustration [PNG]. Pixabay. https://pixabay.com/illustrations/car-yellow-png-967387/
* Kanu, S., & Mane, O. (2024). colors.ppm [PPM Image File]. Licensed under the MIT License. Available from https://github.khoury.northeastern.edu/ommane1/PixelCraft-Image-Editing-and-Enhancement.
