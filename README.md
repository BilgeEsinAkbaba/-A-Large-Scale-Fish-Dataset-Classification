# -A-Large-Scale-Fish-Dataset-Classification

📝 Proje Açıklaması

Bu proje, çeşitli balık türlerini sınıflandırmak için yapay sinir ağı (ANN) modelini kullanmaktadır. Proje, bir büyük ölçekli balık veri seti üzerinde çalışarak, görüntü işleme ve derin öğrenme teknikleri ile farklı balık türlerinin tanımlanmasını amaçlamaktadır.

🐟 Veri Seti

Proje, A Large Scale Fish Dataset isimli bir veri setini kullanmaktadır. Bu veri seti, aşağıdaki balık türlerini içermektedir:

- **Black Sea Sprat**
- **Gilt Head Bream**
- **Horse Mackerel**
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
- **PIL (Pillow)**: Resim işleme için

🏗️ Model Yapısı

Model, aşağıdaki katmanlardan oluşmaktadır:

- **Giriş Katmanı**: 
  - 512 nöron (ReLU aktivasyon fonksiyonu ile)
- **Dropout Katmanı**: 
  - %50 oranında dropout
- **Gizli Katman**: 
  - 256 nöron (ReLU aktivasyon fonksiyonu ile)
- **Dropout Katmanı**: 
  - %50 oranında dropout
- **Gizli Katman**: 
  - 128 nöron (ReLU aktivasyon fonksiyonu ile)
- **Çıkış Katmanı**: 
  - Balık türlerini sınıflandırmak için softmax aktivasyon fonksiyonu ile

📊 Eğitim ve Değerlendirme

Model, eğitim verisi ile 10 epoch boyunca eğitilmiştir. Eğitim ve doğrulama doğruluğu ile kaybı, eğitim süreci boyunca görselleştirilmiştir.

Karışıklık matrisi ve sınıflandırma raporu, modelin performansını değerlendirmek için kullanılmaktadır.
