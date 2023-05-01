# Implementation-of-Erosion-and-Dilation...

## Aim:

To implement Erosion and Dilation using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7,

2. OpenCV.

## Algorithm:

### Step 1:

Load the necessary packages requiured for the implemtation of erosion and dilation on an image.

### Step 2:

Create the text image for the implemtation of erosion and dilation using cv2.putText function.

### Step 3:

Create the structuring image for the implemtation of erosion and dilation on the text image.

### Step 4:

Apply the erosion and dilation to the text image using cv2.erode and cv2.dilate.

### Step 5:

Display the images of the erosion and dilation applied using the plt.imshow.
 
### Step 6:

End the program.

## Program:

```python

Developed by : Anto Richard. S
Register Number: 212221240005
Program to implement Erosion and Dilation using Python and OpenCV.

```

```python

# Import the necessary packages:

import cv2
import numpy as np
import matplotlib.pyplot as plt

```

```python

# Create the Text using cv2.putText:

text_image = np.zeros((100,300),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX = 7
cv2.putText(text_image,"Richard",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Text Image")
plt.imshow(text_image,'magma')
plt.axis('off')

```

```python

# Create the structuring element:

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

```

```python

# Erode the image:

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Text Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

```

```python

# Dilate the image:

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Text Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```

## Output:

### Display the input text Image:

![out1](https://user-images.githubusercontent.com/93427534/235469188-6d26b0dd-c219-4646-86d7-050dbe57ca66.png)

### Display the Eroded text Image:

![out2](https://user-images.githubusercontent.com/93427534/235469199-efcbf874-9f14-4eb3-8310-b2d4ecf9a034.png)

### Display the Dilated text Image:

![out3](https://user-images.githubusercontent.com/93427534/235469212-7231cf5d-20d9-4d9a-af7a-90bfc146bf39.png)

## Result:

Thus the generated text image is eroded and dilated using python and OpenCV.

