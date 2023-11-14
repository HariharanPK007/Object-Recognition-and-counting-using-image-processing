# Object-Recognition-and-counting-using-image-processing'.

This code is a Python script that uses the OpenCV library to detect and label objects in an image. Specifically, it identifies and counts phones, pens, and books in the given image. Below is an explanation of each section of the code along with some details:

## Library Imports

In this segment, essential libraries for image processing are imported. These include OpenCV (cv2) and numpy. Additionally, a function called `cv2_imshow` from the Google Colab library is imported to facilitate image display.

## Phone Detection

This section is dedicated to identifying phones within an image:

1. The image is loaded using the `cv2.imread('sample image.png')` function.
2. The loaded image is then converted to the HSV color space, known for its effectiveness in color-based object detection.
3. Lower and upper color range values are specified to define the acceptable range of hues, saturations, and values for the phone color.
4. A mask is generated to pinpoint regions in the image that match the specified phone color range.
5. Morphological operations (opening) are applied to the mask to refine phone detection.
6. Contours of the identified phone regions are determined.
7. Bounding boxes are drawn around the detected phones, accompanied by corresponding labels.
8. The count of recognized phones is presented alongside the annotated image.

## Pen Detection

This portion is concerned with detecting pens within the image:

1. The image is once again loaded and converted to the HSV color space.
2. Lower and upper color range values are set to define the acceptable range of hues, saturations, and values for the pen color.
3. A mask is created for the pen based on the specified color range.
4. Morphological operations are applied to the pen mask to refine pen detection.
5. Contours of the identified pen regions are determined.
6. Bounding boxes are drawn around the detected pens, accompanied by corresponding labels.
7. The count of recognized pens is presented alongside the annotated image.

## Book Detection

This segment concentrates on detecting books within the image:

1. The image is loaded and converted to the HSV color space.
2. Lower and upper color range values are defined for book covers. Multiple color range definitions are provided to account for different shades of book covers.
3. An initial empty mask for books is created, and masks for different book shades are combined using a bitwise OR operation.
4. Morphological operations are applied to the book mask to refine object detection.
5. Contours of the identified book regions are determined.
6. Bounding boxes are drawn around the detected books, accompanied by corresponding labels.
7. The count of recognized books is presented alongside the annotated image.

## Image Display

At the conclusion of each section, the script utilizes the `cv2_imshow` function to display the image with bounding boxes and labels around the identified objects. To utilize this code, upload it to Google Colab and use the file "sample image.png" for testing.
