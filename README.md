# Image Segmentation with DeepLabV3 & Mask R-CNN

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=flat&logo=opencv&logoColor=white)

## Project Overview
This repository contains a comprehensive implementation of modern **Image Segmentation** techniques using **PyTorch**. The project explores two primary computer vision tasks:
1.  **Semantic Segmentation:** Classifying every pixel in an image into a category (e.g., human vs. background) using **DeepLabV3** with a **ResNet-101** backbone.
2.  **Instance Segmentation:** Detecting distinct objects of interest and generating pixel-wise masks for each instance using **Mask R-CNN**.

The project demonstrates how to load pretrained models, preprocess real-world images, and visualize segmentation masks.

## Models Architectures

### 1. DeepLabV3 (Semantic Segmentation)
* **Backbone:** ResNet-101 pretrained on COCO.
* **Function:** Assigns a label to every pixel. Effective for tasks like "Human Segmentation" where the goal is to separate the person from the background.
* **Key Feature:** Uses Atrous Spatial Pyramid Pooling (ASPP) to capture multi-scale contextual information.

### 2. Mask R-CNN (Instance Segmentation)
* **Backbone:** ResNet-50 with Feature Pyramid Network (FPN).
* **Function:** Detects individual objects and generates a unique mask for each one (e.g., separating two different people in the same image).
* **Key Feature:** Extends Faster R-CNN by adding a branch for predicting segmentation masks.

## Tech Stack
* **Deep Learning Framework:** PyTorch, Torchvision
* **Image Processing:** OpenCV, PIL (Python Imaging Library), NumPy
* **Visualization:** Matplotlib

## Project Structure
* **Task 1:** Loading DeepLabV3 and performing inference on standard images.
* **Task 2:** Human Segmentation using a specific dataset clone (`Human-Segmentation-Dataset`).
* **Task 3:** Instance Segmentation experiments with Mask R-CNN.

## How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PyPro2024/PyTorch-Image-Segmentation-DeepLabV3.git]
    ```
2.  **Install dependencies:**
    ```bash
    pip install torch torchvision numpy matplotlib opencv-python pillow
    ```
3.  **Run the Notebook:**
    Open `DeppLabV3.ipynb` in Jupyter Notebook or Google Colab. The notebook will automatically download the necessary pretrained weights from `torchvision`.

## 🖼️ Results
The notebook includes visualization functions to:
* Overlay segmentation masks on original images.
* Display color-coded class maps (e.g., pink for humans, green for cars).
* Draw bounding boxes for instance detection.

---
*If you find this project helpful for your computer vision learning, feel free to ⭐ the repo!*
