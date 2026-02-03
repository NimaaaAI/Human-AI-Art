# 🎨 AI vs. Human Art Classifier

## 📌 Project Overview
The rise of generative AI has introduced a fascinating challenge: distinguishing between machine-generated imagery and human-made masterpieces. This project implements a **Convolutional Neural Network (CNN)** to automate this distinction. By analyzing visual patterns, textures, and structural logic, the model learns to identify the subtle "digital signatures" of AI algorithms versus the organic nuances of human artistry.

---

## 🎯 Project Aim
The primary objective is to develop a robust binary classifier that remains accurate despite dataset constraints. We focus on:
* **Identification:** Distinguishing synthetic AI outputs from traditional human artwork.
* **Optimization:** Leveraging transfer learning to maximize performance on a limited sample size.
* **Generalization:** Ensuring the model learns stylistic features rather than just memorizing specific images.

---

## 🏗️ Architecture Choice: Why ResNet18?
A critical factor in this project was the **sample size of the dataset**. In deep learning, using a massive model with a small dataset often leads to **overfitting**, where the model "memorizes" the noise instead of "learning" the features.



I selected **ResNet18** as the backbone for the following reasons:
* **Model Efficiency:** Being a "lighter" model (18 layers deep), it has fewer parameters, making it less prone to overfitting on smaller datasets compared to deeper variants like ResNet101.
* **Residual Connections:** The use of **skip connections** helps avoid the vanishing gradient problem, allowing for more stable and efficient training.
* **Pre-trained Advantage:** By using weights pre-trained on ImageNet, the model already understands basic geometry, edges, and textures, requiring only fine-tuning for the art domain.

---

## 🚀 Key Features
* **Kaggle Integration:** Automated data acquisition using `kagglehub`.
* **Smart Preprocessing:** Data augmentation (rotations, flips) to increase training variety.
* **Training Logic:** Includes **Early Stopping** to prevent over-training and save the best-performing model weights.
* **Deep Evaluation:** Uses **Confusion Matrices** and **Classification Reports** to provide a transparent view of model precision and recall.

---

## 🛠️ Tech Stack
* **Language:** Python
* **Framework:** PyTorch & Torchvision
* **Data Handling:** Pandas, NumPy
* **Evaluation:** Scikit-Learn
* **Visualization:** Matplotlib, Seaborn
