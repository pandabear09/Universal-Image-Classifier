# Universal Image Classifier (ResNet-50)

An out-of-the-box image classification application powered by the **ResNet-50** deep residual network architecture initialized with **ImageNet-1K pretrained weights**. Capable of recognizing 1,000 everyday object, animal, vehicle, and scene categories without requiring custom training.

---

## Features
* **Zero-Training Inference:** Uses pretrained ImageNet weights for immediate classification across 1,000 distinct classes.
* **Automated Preprocessing Pipeline:** Handles image loading, resizing to $224 \times 224$ pixels, batch dimension expansion, and model-specific channel normalization (`preprocess_input`).
* **Top-K Confidence Scoring:** Decodes raw logit outputs into human-readable class labels ranked by softmax probability.
* **Format Support:** Works seamlessly with standard image formats (`.jpg`, `.jpeg`, `.png`, `.webp`).

---

## Model Architecture
This project leverages **ResNet-50** (50-layer Residual Network), which introduces skip connections (identity shortcuts) to prevent vanishing gradients in deep convolutional architectures.

* **Backbone:** ResNet-50 (`weights="imagenet"`)
* **Input Resolution:** $224 \times 224 \times 3$ (RGB)
* **Output Space:** 1,000 ImageNet-1K classes

---

## Project Structure
```text
├──  Universal_Image_Classifier.ipynb                 # Main inference / UI script
├── test_images/          # Test images for quick verification
└── README.md               # Project documentation
