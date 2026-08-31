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
