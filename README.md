# 🔬 Skin Lesion Classification and Segmentation using Deep Learning

This project presents a robust AI-driven **multimodal framework** that integrates both **skin lesion image segmentation** and **multi-class classification**, aiming for accurate and early **skin cancer detection**.

### 👨‍💻 Authors
- Aayush Paturkar – Computer Science Engineering, Ramdeobaba University  
- Sarthak Khutafale – Computer Science Engineering, Ramdeobaba University  

---

## 📌 Project Highlights

- **Multimodal Deep Learning**: Combines image processing and patient symptom data
- **Segmentation**: Custom `Se-DPPM-ResUNet` model for precise lesion masking
- **Classification**: Dual-backbone classifier using `EfficientNet-B4` and `DenseNet-169`
- **Attention Mechanisms**: Incorporates CBAM + SE blocks for enhanced feature focus
- **Dataset**: ISIC 2018 (segmentation), ISIC 2019 (classification – 8 classes)
- **Final Accuracy**: 92.10% (Combined model)

---

## 📂 Dataset

- **Segmentation**: [ISIC 2018 Challenge Dataset](https://challenge2018.isic-archive.com/)
- **Classification**: [ISIC 2019 Dataset](https://challenge2019.isic-archive.com/)
- Images are resized and preprocessed (e.g., hair removal, augmentation)

---

## 🧠 Models Used

### 🔹 Segmentation – `Se-DPPM-ResUNet`
- Dense Pyramid Pooling in bottleneck
- Skip connections and upsampling with sigmoid output
- Dice Coefficient: **~89%**

### 🔹 Classification – Dual Backbone CNN
- **EfficientNet-B4** and **DenseNet-169**
- Features concatenated and passed through CBAM + SE attention blocks
- 8-Class Softmax output:
  - MEL (Melanoma)
  - NV (Nevus)
  - BCC (Basal Cell Carcinoma)
  - AK (Actinic Keratosis)
  - BKL (Benign Keratosis)
  - DF (Dermatofibroma)
  - VASC (Vascular Lesion)
  - SCC (Squamous Cell Carcinoma)

---

## 📊 Results

| Model Type       | Precision | Recall | F1-Score | ROC-AUC | Accuracy |
|------------------|-----------|--------|----------|---------|----------|
| Segmentation     | –         | –      | –        | –       | 88.95%   |
| Classification   | 0.87      | 0.86   | 0.865    | 0.91    | 88.00%   |
| **Combined Model** | **0.90**  | **0.89** | **0.895** | **0.93** | **92.10%** |

---

## ⚙️ Preprocessing Techniques

- Grayscale conversion
- Hair removal via morphological operations + TELEA inpainting
- Augmentations: rotation, shear, zoom, brightness, flip
- Resize to `256x256` for segmentation and `224x224` for classification

---

## 🧪 Evaluation

- Optimized using **Adam optimizer**
- Early stopping and dropout used to avoid overfitting
- Accuracy curve shows convergence by epoch 10
- Loss, Precision, Recall, and ROC-AUC used as evaluation metrics

---

## 📌 Key Contributions

- First integrated architecture of its kind for skin lesion detection using ISIC datasets
- Attention-enhanced CNN pipeline ensures focus on lesion regions
- Scalable and efficient — can be adapted to real-world medical systems

---

## 🏁 Conclusion

Our model outperforms several state-of-the-art benchmarks in skin lesion diagnosis. With accurate segmentation and classification, it minimizes manual dependency and improves early detection — making it a promising clinical decision support tool.

---

---

## 🛠 Tech Stack

- Python
- TensorFlow / Keras / PyTorch
- OpenCV, NumPy, Pandas
- Matplotlib, Seaborn (for visualizations)

---

## 📬 Contact

- 📧 paturkaraa_1@rknec.edu

