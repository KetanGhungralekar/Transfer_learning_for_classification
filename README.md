# Transfer Learning on MNIST with PyTorch

This repository implements a transfer learning approach to classify handwritten digits from the MNIST dataset using a pre-trained ResNet-18 model in PyTorch. The model fine-tunes the ResNet-18 architecture to adapt it for the 10-class MNIST dataset.

## Table of Contents
- [Overview](#overview)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Training](#training)
- [Evaluation](#evaluation)
- [License](#license)

## Overview
This project leverages transfer learning, using the pre-trained ResNet-18 model available in PyTorch's `torchvision` library. The final fully connected layer of the ResNet model is replaced to output 10 classes corresponding to the digits 0-9 in the MNIST dataset. The model is trained and evaluated on resized grayscale images converted to 3 channels.

## Model Architecture
- **Base Model:** ResNet-18 (pre-trained on ImageNet)
- **Modifications:** Final fully connected layer replaced with a new layer for 10 classes (MNIST digits)
- **Input Size:** MNIST images are resized to 224x224 and converted from grayscale to 3 channels to match ResNet's input size.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/KetanGhungralekar/Transfer_learning_for_classification.git
    cd Transfer_learning_for_classification
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows, use `env\\Scripts\\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Download the MNIST dataset:
    The MNIST dataset will be automatically downloaded using `torchvision.datasets.MNIST` the first time you run the code.

2. Train the model:
    ```bash
    python train.py
    ```

3. Evaluate the model:
    ```bash
    python evaluate.py
    ```

## Training

The training script will train the model for 5 epochs (configurable) and print the loss for each epoch.
