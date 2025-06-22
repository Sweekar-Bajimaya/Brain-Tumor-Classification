# 🧠 Brain Tumor Classification using Deep Learning

This project involves building a Convolutional Neural Network (CNN) model to classify brain tumors from MRI images into four categories: **Glioma Tumor**, **Meningioma Tumor**, **Pituitary Tumor**, and **No Tumor**.

---

## 📂 Dataset

The dataset consists of MRI images organized into training and test sets, each containing the four classes mentioned above. The images are grayscale or RGB scans of human brains, and the data was cleaned to remove corrupt files.

- **Classes**:
  - Glioma Tumor
  - Meningioma Tumor
  - Pituitary Tumor
  - No Tumor
- **Structure**:
  ├── Train/
│ ├── glioma_tumor/
│ ├── meningioma_tumor/
│ ├── pituitary_tumor/
│ └── no_tumor/

└── Test/
├── glioma_tumor/
├── meningioma_tumor/
├── pituitary_tumor/
└── no_tumor/


---

## 📊 Exploratory Data Analysis

- Verified the number of images per class
- Removed corrupted images
- Visualized sample images for each class

---

## 🧪 Data Preprocessing

- Resized images to a fixed shape
- Normalized pixel values
- Augmented data using transformations:
- Rotation
- Zoom
- Horizontal/Vertical flip
- Brightness adjustment

---

## 🧠 Model Architecture

### 🔧 Custom CNN

- Convolutional Layers + MaxPooling
- Dropout for regularization
- Batch Normalization
- Dense output layer with Softmax activation

### 💻 Transfer Learning

- **Pre-trained Models Used**:
- ResNet50
- VGG16
- Fine-tuned on the tumor classification task
- Feature extraction from pretrained base

---

## 🏋️ Training Details

- Optimizers: SGD, Adam
- Loss Function: Categorical Crossentropy
- Metrics: Accuracy
- Callbacks:
- EarlyStopping
- ReduceLROnPlateau
- ModelCheckpoint

---

## 📈 Evaluation

- Classification Report
- Confusion Matrix
- Accuracy, Precision, Recall, F1-Score

---

## ✅ Results

The model successfully classified brain tumors with high accuracy. The final architecture (with transfer learning) significantly improved results compared to the custom CNN baseline.

*(Insert training graphs or accuracy tables here if available)*

---

## 💡 Future Work

- Further hyperparameter tuning
- Apply advanced augmentation
- Deploy model using Flask or Streamlit
- Integrate Grad-CAM for interpretability
