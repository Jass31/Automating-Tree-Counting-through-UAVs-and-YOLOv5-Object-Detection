
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

     1. Seed
     2. Dead Tree 
     3. Debries

Below you see one of the satellite images and the corresponding labels:
<p align="center">
  <img src='https://github.com/Jass31/Automating-Tree-Counting-through-UAVs-and-YOLOv5-Object-Detection/assets/86398574/e08428ff-878a-47ed-95c1-cb78dcca7823' alt="the satellite images and the corresponding labels" width="300" height="300" >
    <img src='https://github.com/Jass31/Automating-Tree-Counting-through-UAVs-and-YOLOv5-Object-Detection/assets/86398574/1b46fcbc-f07c-402a-b733-49fa744afd04' alt="the satellite images and the corresponding labels" width="300" height="300" >
    <img src='https://github.com/Jass31/Automating-Tree-Counting-through-UAVs-and-YOLOv5-Object-Detection/assets/86398574/b54b2515-0e35-464a-987c-96caa7cc7951' alt="the satellite images and the corresponding labels" width="300" height="300" >
 </p>

## 3. Model Architecture

The YOLOv5s (Small version) model used in this project consists of 157 layers with a total of 7,020,913 parameters. Below is a summary of the model architecture:

### YOLOv5s Architecture Summary

- **Total Layers:** 157
- **Total Parameters:** 7,020,913
- **Total Gradients:** 0
- **Total GFLOPs:** 15.8

### Model Inference

The model takes an input image of size 352x640 pixels and performs object detection. It successfully identifies the following objects in the image:

- 11 Alive Trees
- 1 Dead Tree
- 3 Debris

### Speed Analysis

- **Pre-process Time:** 0.5ms
- **Inference Time:** 73.3ms
- **NMS (Non-Maximum Suppression) Time:** 0.4ms per image at shape (1, 3, 640, 640)

