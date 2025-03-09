# Edge Detection for Face

# Overview

Edge detection plays a crucial role in various image processing applications across multiple fields like autonomous vehicles, medical diagnostics, and industrial equipment monitoring. This project implements various edge detection methods, including Canny, Sobel, Laplacian, K-means, SVM, and Prewitt, specifically tailored for detecting facial features.

The project uses OpenCV to handle images in the BGR (Blue, Green, Red) color format and focuses on detecting edges where there is a sharp contrast in pixel values.

Methods Used
Sobel
The Sobel method uses gradient boosting with two 3x3 convolutional filters. It detects edges along the vertical and horizontal axes, providing flexibility to focus on either direction depending on the use case.

Canny
The Canny edge detector is one of the most widely used methods. It starts by applying Gaussian blur to reduce noise, then identifies edges and applies dilation to enhance the edge detection.

Laplacian
This method uses a grayscale image and applies Gaussian blur to reduce noise. The second derivative is computed using the Laplacian operator to detect rapid changes in intensity, highlighting edges.

HSV (Hue, Saturation, Value)
In this approach, images are converted from BGR to HSV for better detection of skin color. A mask isolates skin regions, and a Gaussian blur is applied. Haar Cascade is used for face detection, and additional masking excludes hair regions.

Robert
This method uses a grayscale image and calculates the gradient magnitude to detect edges. The gradient is normalized for better accuracy.

K-means
The K-means algorithm is an unsupervised machine learning method used for image segmentation. It groups pixels into clusters based on color similarity, effectively dividing the image into distinct regions.

SVM (Support Vector Machine)
In this approach, random pixel samples are selected for training. The model is then trained to predict edges across the entire image by flattening it into a 1D array and applying an SVM classifier.

K-means with Prewitt
This method combines K-means clustering for segmentation and the Prewitt operator for edge detection. The image is first segmented into distinct regions based on color, and then Prewitt's edge detection is applied to highlight the edges in those regions.
