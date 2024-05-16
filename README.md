
# Automating Tree Counting through UAVs and YOLOv5 Object Detection



## 1.Introduction :

Manually counting trees from UAV (Unmanned Aerial Vehicle) images is a laborious task, particularly in dense forest areas where tree crowns overlap. Traditional methods struggle to accurately detect and count trees in such challenging environments. However, advancements in deep learning offer promising solutions to automate this process.

This repository presents an innovative approach to automate tree counting using YOLOv5, a state-of-the-art object detection model, coupled with high-resolution UAV imagery. By leveraging the power of deep learning, our algorithm intelligently detects and counts individual trees even in densely packed areas with overlapping crowns.
## Requirement

    Python 3.11
    PyTorch
    OpenCV
    NumPy
## 2. Dataset & Pre-Processing:

The dataset comprises drone images with dimensions of 1024 × 1024 pixels, accompanied by labeled masks of the same size. These masks are meticulously annotated by analysts using image labeling tools to accurately represent:

     1. Alive Tree
     2. Dead Tree 
     3. Debries

Below you see one of the satellite images and the corresponding labels:
![App Screenshot](https://drive.google.com/file/d/18nnFCF2tzqxp9oVimWG2-iDgR_iwfT5C/view?usp=drive_link)
