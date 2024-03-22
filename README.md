# EXP 5: IMPLEMENTATION-OF-FILTERS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.


## Program:
#### Developed By : LATHISH KANNA.M
#### Register Number: 212222230073
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/fd9bfc33-57f3-4497-a9f3-079255f3d4aa)




ii) Using Weighted Averaging Filter

![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/a6ef0f84-5d8e-4fe8-aca9-02ec57ccf5f6)




iii) Using Gaussian Filter

![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/66ee18ad-3485-4d7b-8d95-0c23cbf5b9b3)




iv) Using Median Filter

![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/b78f0f14-f944-44a3-9efd-9599e859bae8)




### 2. Sharpening Filters

i) Using Laplacian Kernal

![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/53f7ae97-0a3b-4c60-b34f-1592f9be5a13)


ii) Using Laplacian Operator

![image](https://github.com/lathishlathish/Implementation-of-filter/assets/120359170/0613ebc4-39ed-48fd-a021-79a3769159fa)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
