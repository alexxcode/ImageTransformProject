# ImageTransformProject
A colorful journey through C++ image processing. This project will edit the imported PNG image by illinifying, spotlighting, and watermarking it using C++ language.


## Part 1: HSLAPixel
## Understanding Color Spaces
we will not be working with the physical properties of color that you may be familiar with from
other sources (the “RGB color space” for red-green-blue channels.) Instead, we will be using an alternative
color space that represents colors by human perception of color. The HSL color space uses the Hue, Saturation,
and Luminance of the color. From the Adobe Technical Guides page on “The HSB/HLS Color Model”, Adobe
explores these terms:

## Hue
Hue (denoted as h) defines the color itself, for
example, red in distinction to blue or yellow. The
values for the hue axis run from 0–360° beginning
and ending with red and running through green,
blue and all intermediary colors like greenish-blue,
orange, purple, etc.

  
![Hue](https://github.com/alexxcode/ImageTransformProject/blob/main/ImageTransformProject/images/hue.png)

## Saturation
Saturation (denoted as s) indicates the degree to which the hue differs from a neutral gray. The values run from
0%, which is no color saturation, to 100%, which is the fullest saturation of a given hue at a given percentage of
illumination.

![Saturation](https://github.com/alexxcode/ImageTransformProject/blob/main/ImageTransformProject/images/saturation.png)



## Luminance
Luminance (denoted as l) indicates the level of illumination. The values run as percentages; 0% appears black
(no light) while 100% is full illumination, which washes out the color (it appears white).

![Luminance](https://github.com/alexxcode/ImageTransformProject/blob/main/ImageTransformProject/images/luminance.png)


## HSL Color Space
The full HSL color space is a three-dimensional space, but it is not a cube (nor exactly cylindrical). The area
truncates towards the two ends of the luminance axis and is widest in the middle range. The ellipsoid reveals
several properties of the HSL color space:
* At l=0 or l=1 (the top and bottom points of the ellipsoid), the 3D space is a single point (the color black
and the color white). Hue and saturation values don’t change the color.
* At s=0 (the vertical core of the ellipsoid), the 3D space is a line (the grayscale colors, defined only by
the luminance). The values of the hue do not change the color.
* At s=1 (the outer shell of the ellipsoid), colors are vivid and dramatic!

  ![HSL_color_space](https://github.com/alexxcode/ImageTransformProject/blob/main/ImageTransformProject/images/HSL_color_space.png)

  # Part 1 Programming Objectives 
the HSLAPixel class within the uiuc namespace in the file uiuc/HSLAPixel.h . Each
pixel contains four public member variables:
* h , storing the hue of the pixel in degrees between 0 and 360 using a double
* s , storing the saturation of the pixel as a decimal value between 0.0 and 1.0 using a double
* l , storing the luminance of the pixel as a decimal value between 0.0 and 1.0 using a double
* a , storing the alpha channel (blending opacity) as a decimal value between 0.0 and 1.0 using a double
