# boomcamp-project
# 🧠 Brain Tumor MRI Classification with CNN & Eigen-CAM

## 📌 Proje Amacı
Bu proje, MRI görüntülerinden **beyin tümörlerini sınıflandırmak** için bir Convolutional Neural Network (CNN) modeli geliştirmeyi ve modelin kararlarını **Eigen-CAM** yöntemi ile görselleştirmeyi amaçlamaktadır.  

---

## 📂 Veri Seti
- Kullanılan veri seti: [Brain Tumor MRI Dataset (Kaggle)](https://www.kaggle.com/datasets)  
- Veri setinde 4 sınıf bulunmaktadır:
  - **Glioma**
  - **Meningioma**
  - **Pituitary**
  - **Notumor**

Eğitim ve test setleri hazır olarak verilmiştir.  

---

## ⚙️ Kullanılan Yöntemler ve Kütüphaneler
- **Python Kütüphaneleri**:  
  `tensorflow`, `keras`, `numpy`, `pandas`, `matplotlib`, `seaborn`,  
  `opencv-python`, `PIL`, `scikit-learn`  

- **Data Augmentation Teknikleri**:
  - Rotation
  - Shift (yatay/dikey)
  - Zoom
  - Shear
  - Horizontal Flip

- **Callback’ler**:  
  - `EarlyStopping`
  - `ReduceLROnPlateau`
  - `ModelCheckpoint`

📊 Sonuçlar
Test Accuracy: ~%73-75
Precision, Recall ve F1-Score değerleri her sınıf için hesaplanmıştır.
Confusion Matrix ile sınıflar arası hata dağılımları görselleştirilmiştir.
Eigen-CAM yöntemiyle modelin karar verdiği bölgeler görselleştirilmiştir.
📷 Örnek görseller (sen kendi çıktılarını buraya ekleyebilirsin):
Accuracy / Loss grafikleri
Confusion Matrix
Eigen-CAM örnekleri

## Çalıştırma
- Kaggle notebook linki: https://www.kaggle.com/code/remsumt/notebook5785386ede


