# 🔤 Armenian Letter Classifier (Both Uppercase & Lowercase)

This project provides a trained machine learning model that can **classify Armenian letters**, distinguishing between **uppercase and lowercase characters** from the Armenian alphabet.

The model is designed to recognize characters from image inputs and can be used in OCR pipelines, educational tools, or Armenian language processing systems.

## 🧠 Model Overview

- **Type**: Convolutional Neural Network (CNN)
- **Input**: Grayscale image of a single Armenian character (e.g., 28x28 or 64x64)
- **Output**: One of the 76 classes:
  - 39 uppercase Armenian letters (Ա–Ֆ)
  - 39 lowercase Armenian letters (ա–ֆ)
  - Model's accuracy score is 0.95 (95%)

## 📦 Files

- `mashtocimg.h5` – Trained Keras model (HDF5 format)
- `label_map.json` – Mapping of class indices to Armenian letters

## 🧾 Dataset

The model was trained on a custom dataset of handwritten and printed Armenian characters.

- **Total samples**: 70,000+
- **Classes**: 78 (uppercase and lowercase)
- **Balance**: Roughly equal samples per class
- **Format**: 64x64 images

## 🚀 Usage

### Load the model
```python
from tensorflow.keras.models import load_model
import numpy as np
from PIL import Image

model = load_model("mashtocimg.h5")
