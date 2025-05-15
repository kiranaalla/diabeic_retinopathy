# 🧠 Diabetic Retinopathy Detection using Deep Learning (CNN)

This project implements a diabetic retinopathy detection system that classifies retinal fundus images into five severity levels using a Convolutional Neural Network (CNN) model. The goal is to assist ophthalmologists in early detection and treatment planning for diabetic retinopathy.

---

## 📁 About the Dataset

The dataset used includes thousands of high-resolution retina images, labeled by severity of diabetic retinopathy:

Each sample includes:

- 🖼️ `.jpeg` image of a retina
- 🏷️ Label ranging from 0 to 4:
  - 0: No DR
  - 1: Mild
  - 2: Moderate
  - 3: Severe
  - 4: Proliferative DR

The dataset was split into:

- **Training**: 70%
- **Validation**: 20%
- **Testing**: 10%

using a custom data split in the notebook.

---

## ⚙️ Dataset Processing

- **Resizing**: All images resized to 224x224 for CNN compatibility
- **Normalization**: Pixel values scaled between 0 and 1
- **Augmentation**: Includes horizontal flips, rotations, zooms
- **Directory Structure**: Automatically handled by `ImageDataGenerator`

---

## 🛠️ Data Loading & Preprocessing

A custom pipeline loads images using TensorFlow's `ImageDataGenerator`:

- Loads images from folders grouped by class
- Splits into training and validation sets
- Applies real-time data augmentation during training

## 🧠 Model Architecture & Training

We used a custom **Convolutional Neural Network (CNN)** built using **TensorFlow/Keras** for classifying retinal images.

---

### 🔧 Training Configuration

| Parameter         | Value                     |
|------------------|---------------------------|
| Epochs           | 25                        |
| Batch Size       | 32                        |
| Image Size       | 224x224                   |
| Optimizer        | Adam                      |
| Loss Function    | Categorical Crossentropy  |
| Early Stopping   | Yes                       |
| Device           | GPU (if available)        |

---

## 🚀 Evaluation & Results

The model achieved high accuracy in classification on the validation set.

---

### 📊 Performance Metrics (Approx.)

| Metric             | Value                          |
|--------------------|--------------------------------|
| Accuracy           | ~85–90%                        |
| Validation Loss    | Stable after 15–20 epochs      |
| Augmentation       | Improved generalization        |
| ROC-AUC (optional) | Can be added in future         |

---

## 🧪 Testing & Visualization

We tested the model on unseen test data, and visualized results using `matplotlib`:

- 📊 **Accuracy & Loss Curves**
- 🖼️ **Sample Predictions**
- 🧩 **Confusion Matrix** (optional future addition)

---

## 👨‍💻 Contributors

- **Kiran**  
- **sivasai**  
- **sumanth Reddy**

---

## 📌 Future Scope

- 🔁 **Expand Dataset**: More retina images with expert-verified labels  
- 🧠 **Pretrained Models**: Try EfficientNet, ResNet variants  
- 📱 **Mobile Deployment**: Export model using TensorFlow Lite or ONNX  
- 💡 **Explainability**: Integrate Grad-CAM for visualizing attention areas
