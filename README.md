# Colour Detection in Images

## Overview
This project implements color detection in images using OpenCV and NumPy in Python. It reads an image, converts it into different color spaces, and isolates a specific color range using masking techniques. The detected color is highlighted in the output image.

## Features
- Reads and displays an image using OpenCV and Matplotlib.
- Converts the image from BGR to RGB and HSV color spaces.
- Applies color thresholding using NumPy to detect a specified color.
- Uses masking techniques to highlight the detected color.

## Technologies Used
1. **OpenCV**: Used for image processing tasks such as reading images, color space conversion, and applying masks.
2. **NumPy**: Utilized for handling arrays and performing operations like defining color thresholds and bitwise operations.

## Installation
Ensure you have the required libraries installed:
```bash
pip install opencv-python numpy matplotlib
```

## Usage
1. Place the target image (`Colours image.jpeg`) in the `/content/` directory.
2. Run the Python script in a Jupyter Notebook or Google Colab.
3. The script will:
   - Read and display the image.
   - Convert the image to RGB and HSV color spaces.
   - Apply color thresholding to detect a specific color.
   - Display the processed images with the detected color highlighted.

## Code Explanation
1. **Reading the Image**: The image is loaded using OpenCV (`cv2.imread`).
2. **Color Space Conversion**: The image is converted from BGR to RGB (`cv2.COLOR_BGR2RGB`) and then to HSV (`cv2.COLOR_RGB2HSV`).
3. **Color Thresholding**: A specific color range is defined using NumPy arrays (`lower` and `upper` bounds in HSV format).
4. **Masking and Result Generation**: `cv2.inRange()` creates a binary mask, and `cv2.bitwise_and()` applies the mask to extract the desired color.
5. **Displaying the Results**: Matplotlib is used to visualize the original, processed, and masked images.

## Example Output
The script processes the image and highlights the detected color based on the predefined HSV range. The final image will only show the selected color while masking the rest.

## Future Enhancements
- Implementing interactive color selection.
- Allowing users to detect multiple colors simultaneously.
- Enhancing real-time color detection using webcam input.


