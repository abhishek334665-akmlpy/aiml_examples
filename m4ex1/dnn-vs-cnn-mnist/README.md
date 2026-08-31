# DNN vs CNN — MNIST Image Classification

A hands-on TensorFlow/Keras experiment comparing a **fully connected DNN** and a **Convolutional Neural Network (CNN)** on the same MNIST image-classification task.

This notebook is designed as an interview-focused learning exercise for understanding the core CNN concepts rather than optimizing model accuracy.

## Objective

Use the same image data and the same overall ML pipeline with two different architectures:

### Fully Connected DNN

```text
Image → Flatten → Dense → Dense → Softmax
```

### CNN

```text
Image → Conv2D → MaxPooling → Flatten → Dense → Softmax
```

The experiment demonstrates why CNNs are better suited to image data.

## What the notebook demonstrates

- MNIST image representation
- Pixel normalization
- Why a DNN flattens an image
- Why CNNs preserve spatial structure
- `Conv2D`
- convolution filters / kernels
- feature maps
- `MaxPooling2D`
- `Flatten`
- Dense layers
- local connectivity
- parameter sharing
- parameter-count comparison
- training the same task with DNN and CNN
- comparing test accuracy
- comparing predictions on the same images
- visualizing learned CNN feature maps
- Keras Functional API

## Key Learning

The overall ML pipeline does **not** fundamentally change:

```text
Data
 ↓
Preprocessing
 ↓
Train/Test data
 ↓
Build model
 ↓
Compile
 ↓
Train
 ↓
Evaluate
 ↓
Predict
```

The major difference is the **model architecture**.

### DNN

The image is flattened early:

```text
28 × 28
   ↓
Flatten
   ↓
784 values
   ↓
Dense
```

### CNN

The image remains spatially structured while features are extracted:

```text
28 × 28 × 1
   ↓
Conv2D
   ↓
Feature maps
   ↓
Max Pooling
   ↓
Flatten
   ↓
Dense
```

## Why CNN?

Images contain spatial relationships. Nearby pixels are related, and useful patterns such as edges, curves and shapes can appear at different locations.

CNNs exploit this using:

1. **Local connectivity** — convolution filters examine small regions.
2. **Parameter sharing** — the same learned filter is reused across the image.
3. **Pooling** — reduces spatial dimensions while retaining important information.

## Repository Structure

```text
dnn-vs-cnn-mnist/
├── DNN_vs_CNN_MNIST.ipynb
├── README.md
└── requirements.txt
```

## Requirements

- Python 3.x
- TensorFlow 2.x
- NumPy
- Matplotlib

Tested conceptually with TensorFlow 2.21.0.

Install:

```bash
pip install -r requirements.txt
```

## Running the Notebook

Open the notebook in Jupyter Notebook, JupyterLab, or VS Code:

```bash
jupyter notebook DNN_vs_CNN_MNIST.ipynb
```

The first run downloads the MNIST dataset through Keras.

## Important Notes

The notebook intentionally uses only a few epochs. The purpose is **architecture understanding**, not achieving state-of-the-art accuracy.

Exact accuracy and training time can vary depending on:

- CPU/GPU
- TensorFlow version
- hardware
- random initialization
- runtime environment

## Interview Takeaway

A strong concise answer to:

**"What is the difference between a DNN and a CNN for image data?"**

> A fully connected DNN typically flattens an image and processes the pixels through Dense layers. A CNN preserves spatial structure and uses local, shared convolutional filters to learn spatial features efficiently, often followed by pooling and Dense layers for classification.

## Course Context

This project supports the **IITK E&ICT Academy AI/ML — Module 4: Core Machine Learning / Deep Learning with Keras and TensorFlow**, specifically the CNN portion.

It is intentionally focused on **Pass 1 understanding and interview readiness**, not exhaustive mathematical derivation.
