# 🖼️ Analysis on Image Feature Extraction

An implementational study on **traditional and deep learning techniques for image feature extraction** for Hand Sign Language Classification.

This project explores how different feature extraction methods impact classification accuracy on both standard and real-world datasets.

---

## 📌 Project Objective

The main objective of this project is to:

- Extract meaningful features from hand sign images
- Compare traditional feature engineering techniques with deep learning approaches
- Improve classification accuracy using preprocessing and clustering
- Evaluate real-world performance using a custom dataset

---

## 🛠️ Techniques Used

### Image Processing
- Gaussian Smoothing (5×5 kernel)
- Canny Edge Detection
- Data Resizing (128×128 for custom dataset)

### Traditional Feature Extraction
- SIFT (Scale-Invariant Feature Transform)
- SURF (Speeded-Up Robust Features)
- ORB (Oriented FAST and Rotated BRIEF)
- Bag of Visual Words (BoVW)
- K-Means Clustering

### Machine Learning Algorithms
- Multiple classical classifiers tested on extracted features

### Deep Learning
- Custom CNN with Batch Normalization
- Transfer Learning using Inception v3
- ADAM Optimizer
- ReLU Activation
- Dropout Regularization

---

# 🔹 Traditional Feature Detection

Before feature extraction, preprocessing steps were applied:

1. Noise reduction using Gaussian filter (5×5)
2. Edge detection using Canny detector
3. Feature descriptor extraction

Preprocessing improved:
- Feature descriptor quality
- Overall classification accuracy

---

## 📌 Bag of Visual Words (BoVW)

- Extracted descriptors were clustered using K-Means
- Created new feature representations
- Applied classical ML classifiers

> On Sign MNIST dataset: All algorithms achieved **>90% accuracy**

![Traditional Accuracy](images/accuracytrad.png)

---

## 🔍 Feature Extraction Algorithms

### 1️⃣ SIFT

- Handles scale, rotation, affine transformations
- Uses Difference of Gaussian (DoG)
- Robust but computationally expensive

![SIFT 1](images/sift1.png)
![SIFT 2](images/sift2.png)

---

### 2️⃣ SURF

- Faster approximation of SIFT
- Uses box filters and integral images
- Hessian matrix-based detector

![SURF 1](images/surf1.png)
![SURF 2](images/surf2.png)

---

### 3️⃣ ORB

- FAST keypoint detector + BRIEF descriptor
- Rotation invariant
- Efficient and suitable for real-time systems

![ORB 1](images/orb1.png)
![ORB 2](images/orb2.png)

---

# 🧠 Deep Learning Feature Extraction

Traditional handcrafted features were compared with CNN-based automatic feature learning.

---

## 🔹 Custom CNN Model

### Architecture:
- 4 Convolutional Layers
- Max Pooling
- Batch Normalization
- Dropout
- 3 Fully Connected Layers
- Softmax Output Layer

### Results:

| Dataset | Epochs | Accuracy |
|----------|--------|----------|
| Sign MNIST | 50 | 97% |
| Improved Dataset | 100 | 94.5% |
| Improved Dataset | 125 | **98.28%** |

### Feature Map Visualization

![CNN 1](images/cnnfeatureout.png)
![CNN 2](images/cnnfeatureout2.png)
![CNN 3](images/cnnfeatureout3.png)
![CNN 4](images/cnnfeatureout4.png)
![CNN 5](images/cnnfeatureout5.png)

---

## 🔹 Transfer Learning (Inception v3)

- Used pretrained Inception v3 model
- Added custom classification layer
- Cached transfer values for faster training
- Stored intermediate values using pickle

### Result:
- 500 epochs → **95% accuracy**
- Performs well on webcam input

![Prediction](images/pred.png)

---

# 📊 Dataset

## 1️⃣ Sign MNIST Dataset
- 27,455 training samples
- 28×28 grayscale images
- High test accuracy but poor webcam generalization

Dataset Link:
https://www.kaggle.com/datamunge/sign-language-mnist

---

## 2️⃣ Improved Custom Dataset
- Created using webcam
- Static American Sign Language gestures
- Original resolution: 480×640
- Resized to 128×128

Advantages:
- More realistic
- Harder to train
- Better real-world performance

---

# 📈 Key Observations

- Deep learning outperforms traditional feature engineering.
- Gaussian smoothing improves descriptor quality.
- Transfer learning reduces training time significantly.
- Real-world dataset improves deployment robustness.

---

# 🚀 Future Improvements

- Real-time deployment optimization
- Mobile implementation
- Data augmentation for better generalization
- Experimenting with modern architectures (ResNet, EfficientNet)

---

# 🧑‍💻 Author

Rohit Kumar  
MCA Graduate | Machine Learning & Computer Vision Enthusiast  

---

# 📜 License

This project is for academic and research purposes.
