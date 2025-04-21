# PixelCraft-Model.Image-Editing-and-Enhancement

**PixelCraft** is an image processing application that offers a range of tools for manipulating and
enhancing images. The project is designed to allow users to perform common image editing tasks like
flipping, adjusting brightness, applying filters, splitting and combining RGB components, and much
more.

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
* Command-Based Interface: Uses command line to read and execute commands for various image manipulations.

### **Getting Started:**

* Java 8 or higher
* A compatible image viewer for output files (e.g., any photo viewer)

### **Installation:**

1. Clone the repository from GitHub:

```
   git clone https://github.khoury.northeastern.edu/ommane1/PixelCraft-Image-Editing-and-Enhancement.git
```

2. Navigate to the project directory:

```
   cd PixelCraft-Image-Editing-and-Enhancement
   ```

3. Compile the project using your preferred IDE or command line.

### **Running the Application:**

Once the project is compiled, you can run the application and load an image for editing. Use the
built-in commands to perform various actions, including:

* Load an image:

```
  load image-path image-name
  ```

* Save an image:

```
  save image-path image-name
  ```

* Get Component:

```
  red-component image-name dest-image-name.
```

Similar command for green, blue, value, luma, intensity components.

* Flip image horizontally:

```
  horizontal-flip image-name dest-image-name
```

* Flip image vertically:

```
  vertical-flip image-name dest-image-name
```

* Adjust brightness:

```
  brighten increment image-name dest-image-name
 ```

* Split image into its RGB components:

```
  rgb-split image-name dest-image-name-red dest-image-name-green dest-image-name-blue
  ```

* Combine image from its individual components:

```
  rgb-combine image-name red-image green-image blue-image
  ```

* Blur image:

```
  blur image-name dest-image-name
```

* Sharpen image:

```
  sharpen image-name dest-image-name
```

* Get Sepia of image:

```
  sepia image-name dest-image-name
```

* Compress image:

```
  compress percentage image-name dest-image-name
```

* Histogram of an image:

```
  histogram image-name dest-image-name
```

* Color correct an image:

```
  color-correct image-name dest-image-name
```

* Adjust the levels of an image:

```
  levels-adjust b m w image-name dest-image-name
```

* Split preview of an operation:
```
   blur image-name dest-image split p
```
Similarly for sharpen, sepia, luma-component(greyscale), color-correct, levels-adjust

* Run the commands:

```
  run script-file
```

* Sample Command File:
  Below is a sample command file for common image processing tasks. You can copy and paste this file into your system and execute the script using the "run" command to see how various features work:


[basic_test_script_jpeg.txt](test%2Fbasic_test_script_jpeg.txt)

This file demonstrates various image manipulations, including loading, saving, color component extraction, flipping, brightening, splitting and combining RGB components, and applying filters like blur, sharpen, and sepia. You can modify the paths or image names as per your setup.

### **Overview:**

Controllers Package:

    ColorComponent: Enum representing various color components (Red, Green, Blue, Luma, etc.) for image processing.
    CommandParser: Parses and processes commands entered by the user or from a script file.
    Controller: Manages image processing operations like loading, saving, and applying filters and transformations.
    FlipDirection: Enum representing the direction of image flips (Horizontal or Vertical).

Controllers.Commands Package:

    AbstractCommand: Abstract class that provides the basic structure for a command, including argument validation.
    BlurCommand: Command to apply a blur filter to an image.
    BrightenCommand: Command to brighten an image by a specified increment.
    Command: Interface for executing commands.
    CommandHistoryCommand: Command to display the history of all executed commands.
    FlipImageCommand: Command to flip an image either horizontally or vertically.
    HelpCommand: Command to display available commands to the user.
    LoadCommand: Command to load an image from a specified path.
    RGBCombineCommand: Command to combine separate red, green, and blue channel images into one.
    RGBSplitCommand: Command to split an image into its red, green, and blue channels.
    RunCommand: Command to run a script containing multiple commands.
    SaveCommand: Command to save an image to a specified path.
    SepiaCommand: Command to apply a sepia filter to an image.
    SharpenCommand: Command to apply a sharpen filter to an image.
    VisualizeComponentCommand: Command to visualize a specific color component of an image.

Controllers.ImageIOUtil Package:

    ImageLoader: Interface for loading images from a file.
    ImageSaver: Interface for saving images to a file.
    JPEGImageLoader: Loads a JPEG image from a file.
    JPEGImageSaver: Saves an image to a JPEG file.
    PNGImageLoader: Loads a PNG image from a file.
    PNGImageSaver: Saves an image to a PNG file.
    PPMImageLoader: Loads a PPM image from a file.
    PPMImageSaver: Saves an image to a PPM file.

Model Package:

    GenerateSepia: Applies a sepia tone filter to an image.
    Image: Represents an image with its pixel data (width, height, and RGBA values).
    ImageBrightness: Adjusts the brightness of an image.

Model.ImageComponent Package:

    AbstractComponent: Abstract class for extracting a specific color component (red, green, etc.) from an image.
    BlueComponent: Extracts the blue component from an image.
    CombineRGB: Combines red, green, and blue images into one image.
    GreenComponent: Extracts the green component from an image.
    ImageComponent: Interface for extracting color components from images.
    IntensityComponent: Extracts the intensity component from an image.
    LumaComponent: Extracts the luma component from an image.
    RedComponent: Extracts the red component from an image.
    SplitImage: Splits an image into its red, green, and blue components.
    ValueComponent: Extracts the value component from an image.

Model.ImageFilter Package:

    AbstractImageFilter: Abstract class for applying filters to images.
    BlurImageFilter: Applies a blur filter to an image.
    ImageFilter: Interface for image filters.
    SharpenImageFilter: Applies a sharpen filter to an image.

Model.ImageFlipping Package:

    AbstractImageFlipper: Abstract class for flipping images either horizontally or vertically.
    HorizontalFlipper: Flips an image horizontally.
    ImageFlipper: Interface for flipping images.
    VerticalFlipper: Flips an image vertically.

Model.ImageIOUtil Package:

    AbstractImageReader: Abstract class for reading images from files.
    AbstractImageWriter: Abstract class for writing images to files.
    ImageReader: Interface for reading images from files.
    ImageWriter: Interface for writing images to files.
    ReadJPEG: Reads a JPEG image from a file.
    ReadPNG: Reads a PNG image from a file.
    ReadPPM: Reads a PPM image from a file.
    WriteJPEG: Writes an image to a JPEG file.
    WritePNG: Writes an image to a PNG file.
    WritePPM: Writes an image to a PPM file.

View Package:

    ProcessImage: Provides the user interface for the application, allowing users to input commands or run scripts.


### **Testing:**

The project includes a suite of unit tests to ensure correct functionality across different
features. These tests validate:

* Image loading and saving
* Brightness adjustments
* Image flipping
* Image filtering
* Color component visualization

To run the tests:

* Navigate to the test directory.
* Run the tests using your preferred testing framework (e.g., JUnit).

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
