# Canny-Edge-Detection
# Canny Edge Detection using Python
## i)Implementation of the Canny edge detection algorithm on a sample image to obtain the edges.
## Developed By : SYED ABBU REHAN
## Register Number : 212223240165
## Code :
```
import cv2
import numpy as np
image = cv2.imread('flower.jpg', 0)  # Reading the image in grayscale mode
blurred = cv2.GaussianBlur(image, (5, 5), 0)  # 5x5 kernel size, sigma = 0
edges = cv2.Canny(blurred, 100, 200)
cv2.imshow('Original Image', image)
cv2.imshow('Canny Edges', edges)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT :

![Screenshot (49)](https://github.com/Abburehan/Canny-Edge-Detection/assets/138849336/3a65ade5-a7f6-47ef-b7f3-2dc207e0eea8)
![Screenshot (50)](https://github.com/Abburehan/Canny-Edge-Detection/assets/138849336/eaae7f60-0720-4bad-b30a-f781d2e3fef7)


## ii)How do different parameter settings impact the result?
The Canny edge detector works by detecting areas of high gradient (i.e., rapid intensity changes) in the image. It involves several steps, including smoothing with a Gaussian filter to reduce noise, computing gradients, and applying non-maximum suppression to thin the edges, followed by edge linking with hysteresis.

## Different parameter settings can significantly impact the result:
### Thresholds (low and high):
These thresholds determine which edges are considered strong, weak, or non-edges. Lower values lead to more edges being detected, while higher values filter out weaker edges. Adjusting these thresholds can impact the sensitivity of edge detection.

### Gaussian blur kernel size:
The size of the Gaussian blur kernel affects the amount of smoothing applied to the image. Larger kernels result in more smoothing, which can reduce noise but may also blur edges.

### Sigma (standard deviation) for Gaussian blur:
Sigma controls the spread of the Gaussian kernel. Higher values result in more smoothing, while lower values preserve finer details. However, too much smoothing can cause edges to be lost.
