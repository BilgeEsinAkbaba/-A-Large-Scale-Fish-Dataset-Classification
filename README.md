# -A-Large-Scale-Fish-Dataset-Classification

📝 Proje Açıklaması

Bu proje, çeşitli balık türlerini sınıflandırmak için yapay sinir ağı (ANN) modelini kullanmaktadır. Proje, bir büyük ölçekli balık veri seti üzerinde çalışarak, görüntü işleme ve derin öğrenme teknikleri ile farklı balık türlerinin tanımlanmasını amaçlamaktadır.

🐟 Veri Seti

Proje, A Large Scale Fish Dataset isimli bir veri setini kullanmaktadır. Bu veri seti, aşağıdaki balık türlerini içermektedir:

- **Black Sea Sprat**
- **Gilt-Head Bream**
- **Hourse Mackerel**
- **Red Mullet**
- **Red Sea Bream**
- **Sea Bass**
- **Shrimp**
- **Striped Red Mullet**
- **Trout**

Her balık türü, belirli bir klasörde bir araya getirilmiş resimlerden oluşmaktadır.

⚙️ Kullanılan Teknolojiler

- **Python**: Programlama dili
- **TensorFlow/Keras**: Derin öğrenme kütüphanesi
- **NumPy**: Sayısal hesaplamalar için
- **Pandas**: Veri işleme ve analiz için
- **Matplotlib**: Görselleştirme için
- **Seaborn**: Gelişmiş görselleştirme için
- **PIL (Pillow)**: Resim işleme için

🏗️ Model Yapısı

Model, aşağıdaki katmanlardan oluşmaktadır:

- **Giriş Katmanı**: 
  - Görüntüler 128x128 piksel boyutunda olup 3 renk kanalına sahiptir (RGB). Bu görüntüler düzleştirilerek giriş katmanına verilir.
- **İlk gizli Katman**:
  - 512 nöron (ReLU aktivasyon fonksiyonu)
  - %10 oranında Dropout uygulanarak overfitting önlenmiştir.
- **İkinci gizli Katman**:
  - 256 nöron (ReLU aktivasyon fonksiyonu)
  - %10 oranında Dropout uygulanarak overfitting önlenmiştir.
- **Üçüncü gizli Katman**:
  - 128 nöron (ReLU aktivasyon fonksiyonu)
  - %10 oranında Dropout uygulanarak overfitting önlenmiştir.
- **Çıkış Katmanı**: 
  - Balık türlerini sınıflandırmak için softmax aktivasyon fonksiyonu kullanılmıştır.
 
🔍 Model Optimizasyonu
Bu projede modelin doğruluğunu artırmak için farklı epoch, batch size ve dropout oranları denenmiştir. Farklı kombinasyonlar kullanılarak elde edilen sonuçlar analiz edilip, en iyi doğruluk oranına sahip model seçilmiştir.

[Ekran Görüntüsü 1: Epoch 128, Batch size 128, Dropout 0.2]
![image](https://github.com/user-attachments/assets/7db49dd4-8a00-4124-ba91-89d75e0b5fff)

[Ekran Görüntüsü 2: Epoch 32, Batch size 128, Dropout 0.2]
![image](https://github.com/user-attachments/assets/9bc1cf15-06ab-43c7-8181-d61b4711bdd0)

[Ekran Görüntüsü 3: Epoch 32, Batch size 64, Dropout 0.2]
![image](https://github.com/user-attachments/assets/c5261e92-fff1-47bf-8b31-58bbbd865147)

[Ekran Görüntüsü 4: Epoch 32, Batch size 32, Dropout 0.2]
![image](https://github.com/user-attachments/assets/1f9a8924-b0ac-4953-b810-98e16e63adb5)

[Ekran Görüntüsü 5: Epoch 32, Batch size 64, Dropout 0.2]
![image](https://github.com/user-attachments/assets/80264cae-6bdd-4c1a-a004-0e44a25c491f)

[Ekran Görüntüsü 6: Epoch 32, Batch size 64, Dropout 0.3]
![image](https://github.com/user-attachments/assets/4f04404c-818a-4d2e-beeb-d4736cf12ff4)

[Ekran Görüntüsü 7: Epoch 32, Batch size 64, Dropout 0.1]
![image](https://github.com/user-attachments/assets/637a950c-ab4f-4cd4-9d45-e05d8387e1cb)


📊 Eğitim ve Değerlendirme

En yüksek doğruluğa sahip model, eğitim verisi ile 32 epoch boyunca eğitilmiştir. Eğitim ve doğrulama doğruluğu ile kaybı, eğitim süreci boyunca görselleştirilmiştir.

Karışıklık matrisi ve sınıflandırma raporu, modelin performansını değerlendirmek için kullanılmaktadır.

Eğitim Sonuçları:

- **Eğitim doğruluğu**: %91
- **Doğrulama  doğruluğu**: %91
- **Eğitim kaybı**: 0.27
- **Doğrulama kaybı**: 0.28
  
![image](https://github.com/user-attachments/assets/e48afac2-cdcc-4f1c-85e5-0ece39c11ad5)

Modelin performansına dayalı olarak, farklı balık türlerinin başarılı bir şekilde sınıflandırıldığı ve modelin overfitting yapmadığı gözlemlenmiştir.



Kaggle linki= https://www.kaggle.com/code/bilgeesinakbaba/fishclassification
