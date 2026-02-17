SVM Neural networks

# CNN Image Classification - CIFAR-10

Image classification using a custom Convolutional Neural Network on the CIFAR-10 dataset, achieving 82.82% test accuracy.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Accuracy](https://img.shields.io/badge/Accuracy-82.82%25-success.svg)

## Overview

Built a CNN from scratch to classify 60,000 images across 10 categories. Experimented with multiple architectures and used data augmentation to improve generalization.

**Result: 82.82% test accuracy**

## Dataset

CIFAR-10 60,000 color images (32×32), 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck. Downloads automatically via TensorFlow.

## Model Architecture

3-block CNN with increasing filters (32 → 64 → 128), batch normalization, dropout, and data augmentation built into the model pipeline.

## Results

| Class | F1-Score |
|-------|----------|
| Automobile | 0.924 |
| Ship | 0.910 |
| Truck | 0.880 |
| Cat | 0.705 (hardest) |

Overall Test Accuracy: **82.82%**

## Key Findings

- Data augmentation improved accuracy from 65% to 82.82%
- Frog class caused most misclassifications due to green color bias
- 3-block architecture outperformed both simpler and deeper models

## How to Run
```bash
pip install tensorflow scikit-learn numpy matplotlib seaborn pandas jupyter
jupyter notebook SVM_neural_networks.ipynb
```

Dataset downloads automatically (~170MB).

## Technologies

Python, TensorFlow, Keras, Scikit-learn, NumPy, Matplotlib, Seaborn

Note: Dataset will load inside notebook.
