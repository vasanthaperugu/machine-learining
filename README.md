SVM Neural networks

Built and trained a convolutional neural network from scratch to classify images across 10 categories, reaching 82.82% test accuracy against a 75% baseline target. The project covers the full ML pipeline: data preprocessing, augmentation, model design, training with callbacks, and error analysis.

What the project does

The notebook trains a CNN on the CIFAR-10 dataset 60,000 small color images (32×32 px) across 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. The dataset downloads automatically when you run the notebook - no manual setup needed.
It goes through exploring the data and visualizing class distribution, preprocessing (normalization, one-hot encoding), building and training a CNN with data augmentation, evaluating with a confusion matrix and per-class F1 scores, and comparing different architectures to understand what worked and what didn't.

How the model works

Data augmentation is applied during training to prevent overfitting. Each image gets randomly flipped, rotated, zoomed, shifted and contrast-adjusted on the fly so the model never sees the exact same image twice. Without this, accuracy stalled at 65% with clear overfitting. With it, the model hit 82.82%.

Architecture - 3 convolutional blocks, each following the same pattern:
Conv2D -> BatchNormalization -> Conv2D -> BatchNormalization -> MaxPooling -> Dropout
Filter sizes grow from 32 -> 64 -> 128 across the blocks, learning increasingly complex features. BatchNorm keeps training stable, Dropout prevents overfitting at each stage.
Training used Adam (lr=0.001) with two callbacks: EarlyStopping monitors validation loss and restores the best weights, while ReduceLROnPlateau halves the learning rate whenever progress stalls. The model trained for 100 epochs, with the learning rate stepped down 7 times as it plateaued. Best weights came from epoch 96.

How to install and run
Install dependencies:
pip install tensorflow numpy matplotlib scikit-learn seaborn pandas

Run cells from top to bottom. No GPU required, though training will be slow on CPU.

Note: Dataset loaded in notebook.
