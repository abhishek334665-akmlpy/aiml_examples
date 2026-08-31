# DNN vs CNN — MNIST Image Classification

A hands-on TensorFlow/Keras experiment comparing a fully connected Deep Neural Network (DNN) with a Convolutional Neural Network (CNN) on the MNIST handwritten-digit classification dataset.

The project uses the same dataset and overall machine-learning workflow for both models to demonstrate how their architectures differ and why CNNs are particularly effective for image data.

## Objective

Compare two neural-network architectures:

### Fully Connected DNN

```text
Image
  ↓
Flatten
  ↓
Dense
  ↓
Dense
  ↓
Softmax
  ↓
Prediction
```

### CNN

```text
Image
  ↓
Conv2D
  ↓
MaxPooling
  ↓
Flatten
  ↓
Dense
  ↓
Softmax
  ↓
Prediction
```

The experiment focuses on understanding the architectural differences rather than optimizing model performance.

## What This Project Demonstrates

- Loading the MNIST dataset
- Image and pixel representation
- Data normalization
- Flattening image data for a DNN
- Building a fully connected DNN with Keras
- Building a CNN with Keras
- `Conv2D`
- convolution filters
- feature maps
- `MaxPooling2D`
- `Flatten`
- Dense layers
- Softmax classification
- Local connectivity
- Parameter sharing
- Model parameter comparison
- Training and evaluation
- Comparing predictions from DNN and CNN
- Visualizing CNN feature maps
- Using the Keras Functional API

## Dataset

The project uses the **MNIST handwritten digit dataset** provided through TensorFlow/Keras.

MNIST contains:

- 60,000 training images
- 10,000 test images
- 10 digit classes: `0` through `9`
- Image size: `28 × 28`
- Grayscale images

Each image contains pixel values ranging from 0 to 255 before normalization.

## Data Preparation

Pixel values are normalized to the range `[0, 1]`.

The DNN uses images with shape:

```text
28 × 28
```

The CNN uses images with an explicit grayscale channel:

```text
28 × 28 × 1
```

The underlying image data remains the same.

## DNN Architecture

The fully connected DNN uses:

```text
Input: 28 × 28
      ↓
Flatten
      ↓
Dense(128, ReLU)
      ↓
Dense(10, Softmax)
```

The `Flatten` layer converts:

```text
28 × 28
```

into:

```text
784
```

The first Dense layer therefore receives all 784 pixel values.

## CNN Architecture

The CNN uses:

```text
Input: 28 × 28 × 1
      ↓
Conv2D(32, 3×3, ReLU)
      ↓
MaxPooling2D(2×2)
      ↓
Flatten
      ↓
Dense(128, ReLU)
      ↓
Dense(10, Softmax)
```

Unlike the DNN, the CNN does not flatten the image immediately.

The convolution layer first extracts spatial features from local regions of the image.

## DNN vs CNN

### Fully Connected DNN

```text
28 × 28
   ↓
Flatten
   ↓
784 values
   ↓
Dense
   ↓
Prediction
```

The spatial arrangement of the pixels is not explicitly preserved once the image is flattened.

### CNN

```text
28 × 28 × 1
     ↓
  Conv2D
     ↓
Feature Maps
     ↓
 Max Pooling
     ↓
  Flatten
     ↓
   Dense
     ↓
 Prediction
```

The CNN preserves spatial structure while learning useful image features.

## Why CNNs Work Well for Images

CNNs take advantage of important properties of image data.

### 1. Local Connectivity

A convolution filter examines a small region of the image rather than connecting every neuron to every pixel.

For example, a `3 × 3` filter examines a local 3 × 3 region.

### 2. Parameter Sharing

The same convolution filter is reused across different locations of the image.

This allows the network to detect similar patterns wherever they occur.

### 3. Feature Extraction

Convolution layers can learn useful visual patterns.

A simplified progression is:

```text
Pixels
  ↓
Local patterns
  ↓
Feature maps
  ↓
Higher-level features
  ↓
Classification
```

### 4. Pooling

Pooling reduces the spatial dimensions of feature maps while retaining important information.

This helps reduce the amount of data passed to later layers.

## Parameter Comparison

The notebook compares the number of trainable parameters in the DNN and CNN.

For the DNN, the first Dense layer receives:

```text
28 × 28 = 784
```

inputs.

With 128 neurons:

```text
784 × 128 + 128
```

trainable parameters are required.

The first CNN layer instead uses:

```text
3 × 3
```

filters shared across the image.

For a grayscale image and 32 filters:

```text
3 × 3 × 1 × 32 + 32
```

parameters are required.

This demonstrates the parameter-sharing principle used by CNNs.

## Model Training

Both models follow the same general machine-learning workflow:

```text
Load Data
   ↓
Preprocess Data
   ↓
Build Model
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

## Visualization

The notebook visualizes:

1. The original MNIST image
2. The flattened representation used by the DNN
3. CNN feature maps
4. Predictions from both models

The feature-map visualization provides a view of the intermediate representations produced by the convolution layer.

## Technologies

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Jupyter Notebook

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

## Running the Notebook

Open the notebook using Jupyter or VS Code:

```bash
jupyter notebook DNN_vs_CNN_MNIST.ipynb
```

Run the cells from top to bottom.

The MNIST dataset will be downloaded automatically by TensorFlow/Keras when required.

## Repository Structure

```text
dnn-vs-cnn-mnist/
├── DNN_vs_CNN_MNIST.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Key Takeaway

The overall machine-learning workflow remains largely the same for DNN and CNN models.

The important difference is how the image is processed:

```text
DNN:
Image → Flatten → Dense → Prediction

CNN:
Image → Convolution → Pooling → Flatten → Dense → Prediction
```

A fully connected DNN treats the image primarily as a vector of values after flattening.

A CNN preserves spatial structure and uses convolution filters, local connectivity, and parameter sharing to learn spatial features before classification.
