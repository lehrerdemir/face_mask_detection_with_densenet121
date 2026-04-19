# 🎭 Face Mask Detection with DenseNet121

## 📌 Proje Hakkında

Bu proje, derin öğrenme teknikleri kullanılarak görüntüler üzerinden bir kişinin **maske takıp takmadığını tespit etmeyi** amaçlamaktadır. Çalışmada transfer öğrenme yaklaşımı kullanılarak önceden eğitilmiş **DenseNet121** modeli temel alınmıştır.

Model, Kaggle üzerinde bulunan *Face Mask Detection Dataset* kullanılarak eğitilmiş ve performansı çeşitli metriklerle değerlendirilmiştir.

---

## 🎯 Amaç

Bu projenin amacı:

* Görüntülerden maske tespiti yapabilen bir model geliştirmek
* Transfer learning yaklaşımını uygulamak
* Model performansını analiz etmek
* Gerçek dünya uygulamalarına uygun bir sistem oluşturmak

---

## 🧠 Kullanılan Teknolojiler

* Python
* TensorFlow / Keras
* NumPy & Pandas
* Matplotlib
* Scikit-learn

---

## 📂 Veri Seti

Veri seti Kaggle platformundan alınmıştır:

👉 https://www.kaggle.com/datasets/omkargurav/face-mask-dataset

Veri yapısı:

```id="j3zfxk"
data/
 ├── with_mask
 └── without_mask
```

---

## ⚙️ Model Mimarisi

Projede kullanılan model:

* **DenseNet121 (pre-trained - ImageNet)**
* GlobalAveragePooling2D
* Dropout (0.5)
* Dense Katmanlar:

  * 256
  * 256
  * 128
  * 64
* Output: 2 sınıf (Softmax)

---

## 🔄 Veri İşleme

* Veri %80 eğitim/validasyon, %20 test olarak ayrılmıştır
* Eğitim verisine veri artırımı uygulanmıştır:

  * Rotation
  * Shift
  * Zoom
  * Horizontal Flip

---

## 🏋️‍♂️ Eğitim Parametreleri

* Optimizer: Adam
* Learning Rate: 0.001
* Epoch: 100
* EarlyStopping (patience=25)
* ReduceLROnPlateau (patience=5)

---

## 📊 Performans Metrikleri

Model aşağıdaki metriklerle değerlendirilmiştir:

* Accuracy
* Precision
* Recall
* Specificity
* F1-score
* Confusion Matrix
* ROC Curve & AUC

---

## 📈 Sonuçlar

Model, test verisi üzerinde yüksek doğruluk oranı elde etmiş ve maske takılı olup olmadığını başarılı bir şekilde ayırt edebilmiştir.

Transfer learning sayesinde sınırlı veri ile bile güçlü sonuçlar elde edilmiştir.

---

## 💾 Checkpoint & Devam Eğitimi

Model eğitimi sırasında:

* En iyi model ağırlıkları kaydedilir
* Eğitim durursa kaldığı yerden devam edebilir

---

## 🚀 Çalıştırma

1. Notebook’u Jupyter Notebook / Google Colab’da aç
2. GPU aktif et
3. Hücreleri sırayla çalıştır
4. Dataset otomatik indirilecektir

---

## 📁 Proje Yapısı

```id="m9xapn"
.
├── notebook.ipynb
├── README.md
├── results/
└── models/
```

---

## 👨‍🎓 Yazar

**Hüseyin Yunus Demir**
İstanbul Topkapı Üniversitesi
Yapay Zeka Yüksek Lisans

---

## 🔗 Github

👉 http://www.github.com/lehrerdemir/face_mask_detection_with_densenet121
