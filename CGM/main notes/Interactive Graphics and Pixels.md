# Basic components of Interactive Graphic system
- Inputs (Mouse, tablets, multi-tasking devices).
- Processing (storage)
- Display (Output)


### Notes:
**What is a pixel?**
- It is a picture element.
- The smallest addressable unit of a digital image or display, that can be controlled or manipulated.
- Pixels are arranged in a grid of rows and columns.
- Pixels help to implement visual information into a digital standard with which computers and other equivalent electronic devices can process, store, and show images.


# Characteristics of Pixel
- Every pixel in the image is defined by (x, y) coordinate in the screen space.
- Each pixel has a color (RGB - Red, Green, Blue).
- Every pixel contains information about color and brightness or sometimes opacity level. (opacity means how non-transparent an object or pixel is, it is the measure of how much light is blocked by a pixel or object).
- Pixels do not have a fixed physical size, their size depends on the screen resolution and display size.
- Pixels are arranged in a 2-D grid pattern(rows and columns) to form an  image.
- The color depth (bit depth) of a pixel determines how many color it can represent.
- Pixels are stored in frame buffers in a memory, where each pixel's color information is stored.
- Total number of pixels on a screen determines its resolution. (e.g. 1920 x 1080).

**Q. What is pixel resolution?**
- Define how many pixels are used to display an image.

**Types of displays(based on pixels)**
1. Monochrome display - 1 -bit per pixel(black or white).
2. Grey-scale display - 8-bit per pixels(256 shades).
3. Color-display - 24-bit per pixel(16.7 million colors using RGB).

**Bit-depth(color depth)**
The number of bits used to represent a pixel's color. (Bits are used to store pixel data, smallest unit of data).

Common bit-depths are:
1. 1-bit: 2 colors
2. 8-bits: 256 colors.
3. 24-bits: 16.7 million colors(True color - 8 bits for R, G, B each).