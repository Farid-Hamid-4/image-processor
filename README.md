# Image Processor
Two basic image processing algorithms - one for sharpening and one for noise removal - using the Nvidia Warp API. Each algorithm written in a dedicated kernel.

## Features
- The unsharp masking algorithm is used to sharpen the image.
- The mean average filtering algorithm is used for noise removal. 

## Usage
<python3 image.py algType kernSize param inFileName outFileName>

- `algType` is either -s (sharpen) or -n (noise removal).
- `kernSize` is the kernel size - e.g. 3 for 3x3, 5 for 5x5, etc.. It must always be positive and odd.
- `param` is the additional numerical parameter that the algorithm needs - e.g. the scaling value k for unsharp masking. 
- `inFileName` is the name of the input image file.
- `outFileName` is the name of the output image file.