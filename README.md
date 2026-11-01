# WORKSHOP-3-Canny-Edge-Detection

## AIM
To implement edge detection on a grayscale image using OpenCV by applying Gaussian Blur to reduce noise and the Canny Edge Detection algorithm to identify edges in the image.

## ALGORITHM

1. Import the required libraries: OpenCV (`cv2`) and Matplotlib (`pyplot`).
2. Read the input image (`img1.jpeg`) in grayscale mode.
3. Apply Gaussian Blur with a kernel size of (5, 5) to remove noise and smooth the image.
4. Apply the Canny Edge Detection algorithm with lower threshold 50 and upper threshold 150.
5. Create a figure using Matplotlib with two subplots.
6. Display the original grayscale image in the first subplot.
7. Display the detected edges in the second subplot.
8. Add titles, hide the axis, and display the final output.

## PROGRAM

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('img1.jpeg', cv2.IMREAD_GRAYSCALE)

blurred = cv2.GaussianBlur(img, (5,5), 0)

edges = cv2.Canny(blurred, 50, 150)

plt.figure(figsize=(10,5))

plt.subplot(121), plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')

plt.subplot(122), plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')

plt.show()
```

# OUTPUT
<img width="699" height="425" alt="download" src="https://github.com/user-attachments/assets/efea3408-f88d-4271-ab9f-49c34615f8bd" />




## RESULT

Thus, edge detection was successfully performed on the grayscale image using the Canny Edge Detection algorithm. Gaussian Blur was used to reduce noise, and the Canny algorithm detected the edges and displayed them alongside the original image.
