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
  
| Class             | Precision | Recall | F1-score | Support |
|------------------|-----------|--------|----------|---------|
| glioma_tumor      | 1.00      | 0.49   | 0.65     | 181     |
| meningioma_tumor  | 0.64      | 0.65   | 0.64     | 183     |
| normal            | 0.61      | 0.97   | 0.75     | 88      |
| pituitary_tumor   | 0.78      | 0.95   | 0.86     | 169     |

|                  | Accuracy  | Macro Avg | Weighted Avg |
|------------------|-----------|-----------|--------------|
| **Total (621)**  | **0.73**  | 0.76 / 0.76 / 0.73 | 0.78 / 0.73 / 0.72 |

> **Note**: Macro Avg and Weighted Avg rows list precision / recall / f1-score respectively.
  


---

## ✅ Results

The model successfully classified brain tumors with high accuracy. The final architecture (with transfer learning) significantly improved results compared to the custom CNN baseline.

![image](https://github.com/user-attachments/assets/fae068ca-a7bf-475d-aa12-0143e7f2970f)
![image](https://github.com/user-attachments/assets/06dfa944-0648-48a6-b3ec-b659c86456c9)
![image](https://github.com/user-attachments/assets/bc86511a-2050-4301-8766-63c0f30f3945)
![image](https://github.com/user-attachments/assets/0cda53db-ed74-4d5c-a841-ccbf0fcc08a2)



---

## 💡 Future Work

- Further hyperparameter tuning
- Apply advanced augmentation
- Deploy model using Flask or Streamlit
- Integrate Grad-CAM for interpretability
