# Facial Keypoints Detection with CNN

This repository presents a deep learning model for **facial landmark detection** using Convolutional Neural Networks (CNNs). Facial landmarks are distinctive points on the face such as the corners of the eyes, the tip of the nose, and the edges of the mouth. Detecting these keypoints is a core task in computer vision with applications in:

* Face recognition and authentication
* Emotion and expression analysis
* Augmented and virtual reality
* Medical imaging and diagnostics
* Human–computer interaction

---

## Model Overview

The model is designed to learn spatial patterns in grayscale face images and predict the coordinates of 15 facial keypoints (30 values in total).

**Architecture highlights:**

* Multiple convolutional + pooling layers for feature extraction
* Dense layers with dropout to reduce overfitting
* Output layer predicts normalized (x, y) keypoint coordinates

---

## Training Summary

* **Input:** 96×96 grayscale images
* **Loss Function:** Mean Squared Error (MSE)
* **Optimizer:** Adam
* **Data Augmentation:** Horizontal flipping for robustness
* **Epochs:** 150
* **Batch Size:** 64
* **Validation Split:** 20%

**Best results achieved:**

* Training Loss (MSE): 9.37e-04 | MAE: 0.0230
* Validation Loss (MSE): 0.0393 | MAE: 0.0728

Model checkpointing was used to preserve the best validation performance.

---

## Requirements

* Python 3.x
* TensorFlow / Keras
* NumPy
* Pandas
* Matplotlib

---
## Sample Input  

<table>
  <tr>
    <td><img width="300" height="300" alt="sample_input" src="https://github.com/user-attachments/assets/1068ff11-b2fd-48f8-8bdd-0224a66fa213" /></td>
    <td><img width="300" height="300" alt="sample_keypoints" src="https://github.com/user-attachments/assets/d6126c57-dae5-4081-88d5-5cfe6cce37ee" /></td>
  </tr>
</table>


## Sample Output
<img width="860" height="644" alt="sample_output" src="https://github.com/user-attachments/assets/881ac279-a551-44fa-ab94-dfac7c47d071" />


## Example Workflow

1. Provide a 96×96 grayscale image of a face as input
2. The trained model predicts 30 keypoint values
3. Keypoints can be visualized by overlaying them on the face image

---

## Future Improvements

* Extend to colored or higher-resolution images
* Experiment with transfer learning from pretrained CNNs
* Enhance robustness to varied lighting and facial poses

---

