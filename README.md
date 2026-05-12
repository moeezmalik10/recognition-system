🧠 Face Recognition System from Scratch
A lightweight face recognition system built entirely with NumPy — no deep learning frameworks. Implements a two-layer Multilayer Perceptron (MLP) trained from scratch using backpropagation to classify faces by identity.
How It Works

Preprocessing — Images are center-cropped (to reduce background noise), resized to 100×100, flattened to a 30,000-dim vector, and standardized.
Architecture — A fully connected MLP: input (30,000) → hidden (256, sigmoid) → output (N classes, softmax)
Training — Cross-entropy loss minimized via gradient descent with Xavier/Glorot weight initialization over up to 2,000 epochs.
Inference — Predicts the identity of a test image along with a confidence score (%).


Tech Stack


Python · NumPy · Pillow · Matplotlib · Google Colab


Dataset Structure


/MyDrive/test/


├── PersonA/   ← training images


├── PersonB/


├── PersonC/


└── test/      ← test images

Features

No PyTorch / TensorFlow — pure NumPy implementation
Automatic multi-class support (add folders to add identities)
Visual prediction output with confidence score
Runs entirely on Google Colab with Drive integration
