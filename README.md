# Image Processor
This Python project provides functionalities to sharpen or apply noise removal to an image. It utilizes the warp library for efficient parallel computation.

## Prerequisites
- Python 3.x
- NumPy
- Pillow
- Nvidia Warp library

## Algorithms
- The unsharp masking algorithm is used to sharpen the image.
- The mean average filtering algorithm is used for noise removal. 

## Usage
python3 image_processing.py [flag] [kernel_size] [parameter] [input_file] [output_file]

- flag: Specify -n for noise removal or -s for sharpening.
- kernel_size: Size of the kernel for mean filtering or unsharp masking. Must be an odd integer greater than 0.
- parameter: The parameter for unsharp masking. A floating-point value.
- input_file: Path to the input image file.
- output_file: Path to save the processed output image.

## Examples
Noise Removal
To apply noise removal to a grayscale image with a kernel size of 3, run the following command:
- python3 image_processing.py -n 3 0.5 input_image.png output_image.png

Sharpening
To perform image sharpening on a color image with a kernel size of 5 and a parameter of 0.8, run the following command:
- python3 image_processing.py -s 5 0.8 input_image.png output_image.png