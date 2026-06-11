# CNN Image Classification

A Convolutional Neural Network (CNN) built with PyTorch to classify images from the CIFAR-10 dataset.

## Overview

This project implements a 3-layer CNN architecture that classifies 32x32 color images into 10 categories:

`airplane`, `automobile`, `bird`, `cat`, `deer`, `dog`, `frog`, `horse`, `ship`, `truck`

## Model Architecture

| Layer | Details |
|-------|---------|
| Conv2D + ReLU + MaxPool | 3 → 32 filters, 3x3 kernel |
| Conv2D + ReLU + MaxPool | 32 → 64 filters, 3x3 kernel |
| Conv2D + ReLU + MaxPool | 64 → 128 filters, 3x3 kernel |
| Fully Connected + ReLU | 2048 → 256 |
| Fully Connected | 256 → 10 |

## Requirements

- Python 3.x
- PyTorch
- torchvision

## Usage

Open and run `CNN.ipynb` in Jupyter Notebook. The notebook will:

1. Download the CIFAR-10 dataset automatically
2. Apply image transformations (normalization to [-1, 1])
3. Train the CNN for 20 epochs using Adam optimizer and CrossEntropyLoss
4. Evaluate accuracy on the test set

## Training Configuration

- Batch size: 32
- Epochs: 20
- Optimizer: Adam
- Loss: CrossEntropyLoss
