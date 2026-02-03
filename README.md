# 🖐️ LSP Recognition: Towards Inclusive Education through AI

This repository contains the development of a recognition system for **Panamanian Sign Language (LSP)** based on Deep Learning techniques. The primary goal is to bridge communication gaps by providing a technological tool that offers immediate feedback for learning basic signs.

---

## 🚀 Tech Highlights

This project integrates a cutting-edge ecosystem for computer vision and sequence processing:

* **[MediaPipe](https://google.github.io/mediapipe/):** Real-time extraction of *keypoints* (pose, hands, and face).
* **[TensorFlow](https://www.tensorflow.org/) & [Keras](https://keras.io/):** Deep Learning engines for neural network architecture.
* **[LSTM (Long Short-Term Memory)](https://en.wikipedia.org/wiki/Long_short-term_memory):** Used to process the sequential and temporal nature of signs.
* **[OpenCV](https://opencv.org/):** Image processing and video stream management.
* **[NumPy](https://numpy.org/):** Efficient management of datasets in multidimensional array formats (`.npy`).

---

## 🛠️ Methodology and Architecture

The project is divided into three critical stages:

1. **Data Collection:** Creation of a proprietary LSP dataset (5 signs: Hello, How are you, Thank you, You're welcome, I understand), featuring 125 sequences of 30 frames per sign.
2. **Preprocessing:** Implementation of normalization techniques to ensure the model remains independent of the user's position relative to the camera.
3. **Training:** Utilization of recurrent architectures (LSTM) to capture the dynamic movement of signs over time.



---

## 🧬 Data Augmentation Techniques (Keypoint Augmentation)

To compensate for the limited dataset size and improve **robustness and generalization**, the following mathematical transformations were applied directly to the keypoint coordinates:

* **Hand Rotation:** Slightly rotates all keypoints within a **±20°** range, simulating variations in hand orientation.
* **Stretching/Compression:** Modifies hand proportions (making it longer or wider) to mimic anatomical differences between individuals.
* **Perspective Change:** Adjusts keypoint positions as if the camera were at a different angle, simulating various points of view.
* **Joint Rotation:** Slightly alters the relative positions between fingers and joints to reflect natural physical variations in sign execution.



---

## 📊 Key Results

* **Maximum Accuracy:** 0.9921 (Normalized-only model).
* **Selected Model:** The **Data Augmentation model (Accuracy: 0.9206)** was chosen for deployment. Although the numerical accuracy is slightly lower, this model demonstrates superior **overfitting control** and significantly better generalization in real-world environments.

---

## 🔮 Future Work

* **Migration to Transformers:** Exploring attention-based architectures for a deeper understanding of linguistic and temporal context.
* **Dataset Expansion:** Collaborating with the deaf community in Panama to scale the vocabulary and improve dialectal accuracy.

---

### 📝 Credits
Project developed as part of scientific research on technological accessibility and inclusive education in Panama.
