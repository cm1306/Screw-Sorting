# 🔩 Basic Screw Detection (YOLOv8 Exploration)

**Status:** Ongoing / Learning Project  
**Goal:** To understand the fundamental workflow of training a custom object detection model for machine vision applications and apply it in the real world.

## 📌 Project Overview
As part of my self-directed learning in machine vision (in preparation for integrating with a robotic arm), I trained a basic object detection model to identify screws. 

**Note:** I am currently learning the fundamentals of computer vision. The core Python inference script used in this repository was generated with the assistance of DeepSeek AI. My primary focus for this project was understanding the *machine vision pipeline*: dataset creation, annotation, model training, and performance evaluation.

**Detection Output**
These images show the YOLOv8 model successfully identifying screws (the small dataset size currently limits precision).
![WhatsApp Image 2026-03-24 at 23 44 29](https://github.com/user-attachments/assets/b8deda53-ded0-4dd8-87d7-c90e37893811)
![WhatsApp Image 2026-03-24 at 23 44 29 (1)](https://github.com/user-attachments/assets/bffda0bf-f099-4b67-9f8c-8d32e4834f84)

## 🎥 Demonstration
*[(https://youtube.com/shorts/NuwBVZz38C4?feature=share)]*


## 📊 Dataset & Training Details
* **Model:** YOLOv8 (Ultralytics)
* **Dataset Size:** 30 training images, 3 validation images, and 2 test images.
* **Performance:** ~0.73 mAP (Mean Average Precision).

## 🧠 Evaluation & Lessons Learned
The current model successfully detects screws, but the precision and recall are relatively low. Through this project, I learned firsthand why data quality is the most critical part of machine vision. 

**Reasons for low precision (0.73 mAP):**
1.  **Extremely Small Dataset:** 35 images are insufficient for robust deep learning.
2.  **Lack of Variation:** The model struggles if the lighting, background, or camera angle changes slightly from the training set.

**Future Improvements:**
If I were to deploy this on a physical hardware system, I would need to:
* Dramatically increase the dataset size (ideally 500+ images).
* Apply Data Augmentation (rotation, exposure changes, noise) to make the model more robust.
* Control the physical environment (e.g., using a ring light and a solid-colored sorting tray) to simplify the visual data.
