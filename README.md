# Introduction to Computer Vision

My first hands-on computer vision project explores how images can be
loaded, represented as numerical data, and transformed using Python.

## Overview

Computer vision is a field of artificial intelligence that enables
computers to extract useful information from images and videos. Images
are represented as arrays of pixel values, which can be inspected and
transformed using image-processing libraries.

This notebook introduces basic image processing operations, including:

-   Loading and displaying an image.
-   Accessing the red, green, and blue (RGB) color channels.
-   Converting an RGB image to grayscale.
-   Converting an image from RGB to HSV and examining its hue,
    saturation, and value channels.

## Technologies Used

-   **Python** --- programming language.
-   **NumPy** --- numerical arrays and image data manipulation.
-   **Matplotlib** --- loading and visualizing images.
-   **OpenCV (`cv2`)** --- image color-space conversions.
-   **Jupyter Notebook** --- interactive environment for running the
    examples.

## Project Structure

``` text
.
├── computer_vision.ipynb   # Notebook containing the image-processing exercises
├── clae.jpg                # Input image used by the notebook
└── README.md               # Project documentation
```

Make sure `clae.jpg` is available in the same directory as the notebook,
or update the image path in the code to match its location.

## Getting Started

### 1. Clone or download the project

If the notebook is stored in a Git repository, clone it and move into
the project directory:

``` bash
git clone <repository-url>
cd <repository-directory>
```

Replace the placeholders with the repository's actual URL and directory
name. If you downloaded the files directly, open a terminal in the
folder containing the notebook.

### 2. Set up a Python environment

Create and activate a virtual environment:

``` bash
python -m venv .venv
```

On Linux or macOS:

``` bash
source .venv/bin/activate
```

On Windows:

``` powershell
.venv\Scripts\Activate.ps1
```

### 3. Install the dependencies

``` bash
pip install numpy matplotlib opencv-python jupyter
```

### 4. Launch the notebook

``` bash
jupyter notebook computer_vision.ipynb
```

Run the cells in order, starting with the imports and then the
image-loading and transformation examples.

## What the Notebook Demonstrates

### 1. Importing libraries

The notebook imports NumPy, Matplotlib, and OpenCV to support numerical
operations, image display, and image transformations.

### 2. Loading and displaying an image

The image is loaded from `clae.jpg` with Matplotlib and displayed
without axis labels. The loaded image is stored as a NumPy array.

### 3. Exploring RGB channels

An RGB image contains separate red, green, and blue channels. The
notebook extracts these channels so their pixel values can be inspected
individually.

### 4. Converting to grayscale

OpenCV converts the RGB image into a single-channel grayscale image:

``` python
gray_image = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)
```

Grayscale represents brightness without displaying separate color
channels.

### 5. Exploring HSV color space

The notebook converts the image from RGB to HSV:

``` python
hsv = cv2.cvtColor(img, cv2.COLOR_RGB2HSV)
```

The resulting channels represent:

-   **Hue:** the type of color.
-   **Saturation:** the intensity or vividness of the color.
-   **Value:** the brightness of the color.

Visualizing these channels helps illustrate how the same image can be
represented in different color spaces.

## Learning Goals

By working through this notebook, you can practise:

-   Loading image files into Python.
-   Understanding images as arrays of pixel values.
-   Extracting and visualizing color channels.
-   Applying basic color-space transformations with OpenCV.
-   Comparing RGB, grayscale, and HSV representations.

## Notes and Troubleshooting

-   **Image not found:** Confirm that `clae.jpg` is in the notebook's
    working directory, or change the path passed to `mpimg.imread()`.
-   **Import errors:** Activate the correct Python environment and
    install the dependencies listed above.
-   **Color conversion:** The conversion code uses `cv2.COLOR_RGB2GRAY`
    and `cv2.COLOR_RGB2HSV`, which match an image loaded with Matplotlib
    as an RGB array. If you load the image with OpenCV instead, note
    that OpenCV normally loads color images in BGR order.
-   **Channel visualization:** To display the extracted channels
    correctly, use the matching variables (`r`, `g`, and `b`) for the
    red, green, and blue plots.

## Future Improvements

Possible next steps include correcting and refining the individual
RGB-channel visualizations, comparing color spaces side by side,
experimenting with additional images, and exploring operations such as
resizing, blurring, edge detection, and thresholding.

## Author

**Claire**

This is an introductory learning project focused on the fundamentals of
image processing and computer vision.
