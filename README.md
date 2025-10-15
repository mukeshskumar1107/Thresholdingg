# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

Step1:
Load the necessary packages.

Step2:
Read the Image and convert to grayscale.

Step3:
Use Global thresholding to segment the image.

Step4:
Use Adaptive thresholding to segment the image.

Step5:
Use Otsu's method to segment the image and display the results

## Program

# Load the necessary packages

```
import cv2
import matplotlib.pyplot as plt
```

# Read the Image and convert to grayscale

```
image=cv2.imread("C:\\Users\\admin\\Downloads\\download (7).jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```

```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)

adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)

_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```


# Use Global thresholding to segment the image

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

```


# Use Adaptive thresholding to segment the image

```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

```

# Use Otsu's method to segment the image 

```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

```

# Display the results


## Output

### Original Image

<img width="795" height="309" alt="image" src="https://github.com/user-attachments/assets/b60500f1-47ae-473e-9bbf-ce9148c22117" />


### Global Thresholding

<img width="889" height="309" alt="image" src="https://github.com/user-attachments/assets/27c52d7b-861b-4b34-a97b-c53363f3f545" />


### Adaptive Thresholding

<img width="813" height="313" alt="image" src="https://github.com/user-attachments/assets/dca6c57e-bae6-42bb-8a80-a36763c228e7" />


### Optimum Global Thesholding using Otsu's Method

<img width="1014" height="312" alt="image" src="https://github.com/user-attachments/assets/46660c77-1783-447d-a9a5-b2102069a084" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
