# Drawing Bounding Boxes with cv2
A bbox labelling function to draw boundaries around objects, including text.

# Before you get started
Knowledge of python 3.6.5 and cv2 library

# Setup
**How to obtain this repository:**
```sh
git clone https//link.to.this.projects.git-repo
```
**Modules/dependencies:**
- `opencv-python`

Install the following dependences:
```sh
pip install opencv-python
```

# Usage
```python
# Import modules
import cv2
from matplotlib import pyplot as plt

# Read in image (note default mode is BGR, to convert to RGB use cvtColor)
image = cv2.imread('./00a87e911c965a90.jpg')
rgb_image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Use draw_rects() function to cast bounding boxes and text on image
image_draw = draw_rects(rgb_image, 
                        [(200,200, 245, 300),
                        (50,50, 120, 80),
                        (500,200, 245, 300)], 
                        'junk food', 
                        y_offset=20, 
                        border_colour=(33, 33, 183),
                        text_bg_colour=(33, 33, 183))

# Plot for verification purposes
plt.figure(figsize=(15,13))
plt.imshow(image_draw)
```

# Tests
- Testing drawing bounding box with text on sample image successfully.
![Image](https://github.com/danielc92/cv2-drawing-boundingboxes/blob/master/result-cropped.jpg)

# Contributors
- Daniel Corcoran

# Sources
