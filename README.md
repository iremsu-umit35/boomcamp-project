# boomcamp-project
# 🧠 Brain Tumor MRI Classification with CNN & Eigen-CAM)
Bu proje, Manyetik Rezonans Görüntüleme (MRI) taramalarından elde edilen beyin tümörü görüntülerinin Dört farklı sınıf (Pituiter, Meningioma, Glioma ve Tümör Yok) arasında sınıflandırılması için bir Evrişimsel Sinir Ağı (CNN) modeli geliştirmeyi amaçlamaktadır.

🎯 Proje Amacı
Temel amaç, klinik teşhis süreçlerine yardımcı olmak amacıyla, verilen bir beyin MR görüntüsünün hangi tümör tipine ait olduğunu veya tümör içermediğini yüksek doğrulukla tespit edebilen robust bir derin öğrenme modeli oluşturmaktır.
Bu proje, MRI görüntülerinden **beyin tümörlerini sınıflandırmak** için bir Convolutional Neural Network (CNN) modeli geliştirmeyi ve modelin kararlarını **Eigen-CAM** yöntemi ile görselleştirmeyi amaçlamaktadır.  

---

## 📂 Veri Seti
- Kullanılan veri seti: [Brain Tumor MRI Dataset (Kaggle)](https://www.kaggle.com/datasets)  
- Veri setinde 4 sınıf bulunmaktadır:
  - **Glioma**
  - **Meningioma**
  - **Pituitary**
  - **Notumor**
- Görseller farklı boyutlarda olup model giriş boyutu **224x224 piksel** olarak yeniden boyutlandırılmıştır.  
Eğitim ve test setleri hazır olarak verilmiştir.  

---

## 🛠️ Kullanılan Yöntemler ve Kütüphaneler
- **Python 3**  
- **TensorFlow / Keras** → Model geliştirme  
- **Matplotlib, Seaborn** → Veri görselleştirme  
- **OpenCV, PIL, NumPy** → Görüntü işleme  
- **ImageDataGenerator** → Data Augmentation  
- **Scikit-learn** → Confusion Matrix & Classification Report  

 
  - 
  - ## 🧩 Model Mimarisi
Model sıfırdan tasarlanmış bir **CNN mimarisi** üzerine kuruludur:

- **Conv2D + BatchNormalization + MaxPooling + Dropout** blokları  
- Filtre sayıları: 32 → 64 → 128 → 256  
- **Flatten → Dense(512, 256)** katmanları  
- Çıkış katmanı: **Softmax (4 sınıf)**  

📌 **Eğitim Parametreleri:**  
- Optimizer: **Adam (lr=0.001)**  
- Loss: **Categorical Crossentropy**  
- Metricler: **Accuracy, Precision, Recall**  


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


