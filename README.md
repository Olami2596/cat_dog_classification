# 🐱🐶 Cat vs. Dog Image Classifier using Transfer Learning

A Jupyter Notebook for classifying cat and dog images using **transfer learning** with **MobileNet V2** and **EfficientNet**, achieving over **97% accuracy** on a balanced dataset of 25,000 images.

---

## 📌 Key Features

* ✅ Utilizes **pre-trained models** from TensorFlow Hub (EfficientNet & MobileNet V2).
* 📦 Works with the **Dogs vs. Cats** Kaggle dataset (25,000 images).
* 📐 Resizes and normalizes images for model input.
* 📊 Achieves **97.67% accuracy** with EfficientNet on a 3K image subset.
* 🖼️ Includes **image prediction and visualization** functionality.

---

## 📁 Dataset

* Source: [Kaggle - Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats)
* 25,000 total images:
  * 12,500 cat images (`cat.#.jpg`)
  * 12,500 dog images (`dog.#.jpg`)
* Balanced dataset ideal for binary classification

To access the dataset, ensure your Kaggle API is set up and run the notebook's download script.

---

## ⚙️ Workflow Overview

### 1. **Data Setup**

* Downloads and extracts the Kaggle dataset (\~812 MB).
* Prepares 25,000 images for preprocessing.

### 2. **Preprocessing**

* Selects 3,000 images (1,500 cats, 1,500 dogs).
* Resizes images to **224x224 pixels**, converts to RGB.
* Normalizes pixel values to \[0, 1].

### 3. **Model Building & Training**

* Loads **EfficientNet** and **MobileNet V2** from TensorFlow Hub.
* Freezes pre-trained layers and adds custom classifier.
* Compiles with **Adam optimizer** and **Sparse Categorical Crossentropy**.
* Trains for **5 epochs** on a train/test split (80/20).

| Model        | Test Loss | Test Accuracy |
| ------------ | --------- | ------------- |
| MobileNet V2 | 0.0531    | 97.33%        |
| EfficientNet | 0.0493    | 97.67%        |


### 4. **Prediction & Inference**

* Accepts custom image input via file path.
* Preprocesses the image and returns classification (Cat/Dog).
* Visualizes the image and confidence level.

---

## 🧪 Requirements

Install the required packages:

```bash
pip install numpy matplotlib scikit-learn tensorflow tensorflow-hub opencv-python Pillow
```

Other prerequisites:

* Python 3.x
* Jupyter Notebook
* Kaggle API key setup

---

## 🔍 Limitations & Improvements

* Only a **subset (3,000 images)** used; training on full dataset may improve accuracy.
* EfficientNet might reuse MobileNet’s model link – requires validation.
* Warnings during compilation hint at possible loss/activation mismatch.

---

## 🚀 Get Started

Clone the repo and launch the notebook in Jupyter or Google Colab to begin classifying cats and dogs with state-of-the-art accuracy!

```bash
git clone https://github.com/yourusername/cat-dog-classifier.git
```



