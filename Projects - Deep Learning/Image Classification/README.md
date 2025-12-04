# 🐶🐱 Cat vs Dog Image Classification using Deep Learning

A complete Deep Learning project built to accurately classify whether an image contains a **Cat 🐱** or a **Dog 🐶** using **Convolutional Neural Networks (CNNs)**. This project uses model training, evaluation, and prediction pipelines with real image datasets.

---

## 📌 Project Overview

The objective of this project is to train a CNN model to automatically differentiate between cat and dog images.  
It includes:

✔ Image preprocessing and augmentation  
✔ CNN model architecture and training  
✔ Performance evaluation  
✔ Real-time image prediction  

---

## 🛠️ Tech Stack

| Category | Tools |
|---------|------|
| Language | Python 3.x |
| DL Framework | TensorFlow / Keras |
| Data Processing | OpenCV, NumPy |
| Model Evaluation | Matplotlib |
| Environment | Google Colab / Jupyter Notebook |

---

## 📥 Dataset Download

This project uses the **Dogs vs Cats** image dataset for training and evaluation.

🔗 Download Dataset from Kaggle:  
<https://www.kaggle.com/datasets/salader/dogsvscats>

### 📌 After Downloading

1. Extract the dataset
2. Place the images inside the `content/` directory following this structure:

📁 Folder Structure:
content/
┣ train/
┃ ┣ cats/
┃ ┗ dogs/
┗ test/
  ┣ cats/
  ┗ dogs/

📎 *Note:*  
Due to the large size (~1GB+), the dataset is **not included** in this repository.  
Please download it manually using the link above.

You have to use **Kaggle Cats vs Dogs dataset**.

---

## 🔧 Project Workflow

### 🔹 1. Data Preprocessing

- Image resizing (150×150)
- Pixel normalization
- Train-Validation split
- Data Augmentation
  - Rotation
  - Zoom
  - Horizontal Flip

### 🔹 2. CNN Model Development

- Multiple Conv2D + MaxPooling layers
- Dense layers with Dropout for regularization
- Sigmoid output for binary classification

### 🔹 3. Model Evaluation

- Accuracy & Loss metrics
- Validation accuracy monitored during training
- Best model saved using ModelCheckpoint

### 🔹 4. Prediction System

- Accepts a single input image
- Outputs class label with confidence

---

## 🧠 Model Performance

✔ Successfully distinguishes Cats & Dogs  
✔ High validation accuracy achieved  
✔ Model generalizes well on unseen images  

📈 *Accuracy and loss graphs can be generated and included for detailed results*

---

## 📊 Model Results

After training the CNN model, we achieved the following performance:

|        Metric       |    Score   |
|---------------------|------------|
| Training Accuracy   | **94.40%** |
| Validation Accuracy | **80.34%** |

✨ The model demonstrates strong learning with good generalization to unseen data.

### 📜 License

This project is open-source and free to use for research and learning purposes.
