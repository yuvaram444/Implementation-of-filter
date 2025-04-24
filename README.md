# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   : YUVARAM. S
### Register Number: 212224230315
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("C:/Users/admin/OneDrive/Pictures/Screenshots/thanjai.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()



```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```
iv)Using Median Filter
```Python

median=cv2.medianBlur (src=image2, ksize=11)
plt.imshow(median)
plt.title(' Median Blurring Filtered')



```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()




```
ii) Using Laplacian Operator
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
</br>![Screenshot 2025-04-24 091302](https://github.com/user-attachments/assets/a9aedaf7-e36b-418b-8066-b63fb49a7dae)

</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
</br>![Screenshot 2025-04-24 091317](https://github.com/user-attachments/assets/d32ea197-ec09-41e8-be6d-4b2a7ed17e5e)

</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
</br>![Screenshot 2025-04-24 091327](https://github.com/user-attachments/assets/b4135b3c-319b-4436-ad28-bf6ce4398b4c)

</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>![Screenshot 2025-04-24 091615](https://github.com/user-attachments/assets/02598f6b-a488-4d9c-abcc-261c4fb64b08)

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>![Screenshot 2025-04-24 091628](https://github.com/user-attachments/assets/a940528c-06a5-4291-851d-f21443f2e4ea)

</br>

ii) Using Laplacian Operator
</br>
</br>
</br>![Screenshot 2025-04-24 091639](https://github.com/user-attachments/assets/249ddce2-e6a4-4824-8621-911fc9d0e931)

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
