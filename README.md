# EXP. 9 – MORPHOLOGICAL OPERATIONS USING OPENCV

**NAME:** NIKILA D  
**REG NO:** 212224230187

## Aim

To implement morphological operations such as Erosion and Dilation using OpenCV and Python to study their effects on an image.

## Software Requirements

- Python
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib

## Morphological Operations

- Erosion
- Dilation

## Algorithm

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Create a blank image of size 500 × 500 with three colour channels.
3. Add the text "Hello World" to the image using `cv2.putText()`.
4. Display the input image with text.
5. Create a 3 × 3 kernel using `np.ones()`.
6. Apply Erosion using `cv2.erode()` to shrink the foreground regions.
7. Display the eroded image.
8. Apply Dilation using `cv2.dilate()` to expand the foreground regions.
9. Display the dilated image.

## Implementation

### 1. Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Create a Blank Image

```python
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

### 3. Add Text on the Image

```python
font = cv2.FONT_HERSHEY_SIMPLEX

cv2.putText(
    image,
    'Hello World',
    (100, 250),
    font,
    1,
    (255, 255, 255),
    2,
    cv2.LINE_AA
)
```

### 4. Display the Input Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
```

**OUTPUT:**

<img width="668" height="572" alt="image" src="https://github.com/user-attachments/assets/462cca6b-ea0a-4103-951c-d1da3b29789e" />

### 5. Create a Kernel

```python
kernel = np.ones((3, 3), np.uint8)
```

### 6. Apply Erosion

```python
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```

**OUTPUT:**

<img width="645" height="562" alt="image" src="https://github.com/user-attachments/assets/208b406a-0012-4106-a017-33a0aa6a0c14" />

### 7. Apply Dilation

```python
dilated_image = cv2.dilate(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
```

**OUTPUT:**

<img width="712" height="570" alt="image" src="https://github.com/user-attachments/assets/f90783ba-f69d-4f08-a9a2-b3ffc634e5f3" />

## Result

Thus, morphological operations such as Erosion and Dilation were successfully implemented using OpenCV and Python. Erosion reduces the foreground regions, whereas Dilation expands the foreground regions in the image.
