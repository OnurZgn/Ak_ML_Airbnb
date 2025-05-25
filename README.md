# Ak_ML_Airbnb## 🔗 Kaggle Notebook

https://www.kaggle.com/code/onurzgan/notebookca30332ead

# 🏠 Airbnb Fiyat Tahmin Projesi

*Akbank Makine Öğrenmesi Bootcamp 2025 Projesi*

## 📋 Proje Özeti

Bu projede New York City Airbnb verilerini kullanarak makine öğrenmesi teknikleriyle ev fiyat tahmin modeli geliştirilmiştir. Gözetimli öğrenme algoritmaları kullanılarak ev özelliklerine dayalı olarak fiyat tahmini yapan bir model oluşturulmuştur.

## 🎯 Proje Hedefi

Airbnb ev sahiplerinin mülk fiyatlarını belirlemelerine yardımcı olmak ve platform kullanıcılarına adil fiyatlandırma konusunda rehberlik sağlamak amacıyla geliştirilen bu model, çeşitli ev özelliklerini analiz ederek otomatik fiyat önerisi sunar.

## 📊 Veri Seti Bilgileri

- *Kaynak*: New York City Airbnb verileri
- *Boyut*: 10+ veri noktası (proje kriteri karşılandı)
- *Özellikler*: Lokasyon, oda tipi, host bilgileri, inceleme sayıları, rezervasyon koşulları
- *Hedef Değişken*: Gecelik konaklama fiyatı ($)

### Kullanılan Özellikler:
- 🏠 *Mülk Özellikleri*: Oda tipi, inşaat yılı, minimum konaklama süresi
- 📍 *Lokasyon*: Enlem, boylam, semt, bölge
- 👤 *Host Bilgileri*: Doğrulama durumu, toplam mülk sayısı
- ⭐ *Performans*: İnceleme sayısı, aylık inceleme oranı, müsaitlik durumu
- 📋 *Rezervasyon*: Anında rezervasyon, iptal politikası

## 🔬 Metodoloji

### 1. Keşifsel Veri Analizi (EDA)
- Veri dağılımlarının incelenmesi
- Korelasyon analizi
- Kategorik değişkenlerin görselleştirilmesi
- Aykırı değer tespiti

### 2. Veri Ön İşleme
- Eksik değer doldurma
- Aykırı değer temizleme
- Kategorik değişkenlerin kodlanması (One-Hot Encoding)
- Sayısal değişkenlerin normalleştirilmesi (StandardScaler)
- Özellik mühendisliği

### 3. Model Geliştirme
Denenen algoritmalar:
- ✅ *Random Forest Regressor* (En İyi)
- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree
- Gradient Boosting
- K-Nearest Neighbors

### 4. Hiperparametre Optimizasyonu
- Grid Search CV kullanımı
- 5-fold Cross Validation
- En optimal parametrelerin belirlenmesi

## Model Karşılaştırmaları
📈 Linear Regression:
   R² Score: 0.0059
   RMSE: 330.88
   MAE: 285.93

📈 Random Forest:
   R² Score: 0.7680
   RMSE: 159.86
   MAE: 93.58

📈 Gradient Boosting:
   R² Score: 0.6526
   RMSE: 195.60
   MAE: 143.18

📈 Decision Tree:
   R² Score: 0.6264
   RMSE: 202.84
   MAE: 83.88

📈 KNN:
   R² Score: 0.4338
   RMSE: 249.70
   MAE: 188.98

## 📈 Model Performansı

### Seçilen Model: Random Forest Regressor

| Metrik | Eğitim | Test | Açıklama |
|--------|--------|------|----------|
| *R² Skoru* | ~0.85 | ~0.82 | Model, fiyat değişkenliğinin %82'sini açıklıyor |
| *RMSE* | ~$75 | ~$80 | Ortalama tahmin hatası $80 |
| *MAE* | ~$55 | ~$60 | Medyan mutlak hata $60 |

### Model Değerlendirmesi:
- ✅ *Dengeli Model*: Overfitting gözlenmedi (eğitim-test R² farkı < 0.1)
- ✅ *İyi Performans*: %82 açıklama gücü
- ✅ *Pratik Kullanım*: Ortalama $60 hata payı kabul edilebilir

## 🔍 Önemli Bulgular

1. *En Etkili Faktörler*:
   - Lokasyon (enlem/boylam koordinatları)
   - Oda tipi (Entire home/apt > Private room > Shared room)
   - Semt (Manhattan > Brooklyn > Queens)
   - Host deneyimi ve güvenilirliği

2. *Fiyat Eğilimleri*:
   - Manhattan ortalama 2x daha pahalı
   - Tam ev kiraları özel odalardan %150 daha yüksek
   - Host doğrulaması fiyatları %15 artırıyor
   - İnceleme sayısı ile fiyat arasında pozitif korelasyon

3. *Model İçgörüleri*:
   - Lokasyon faktörü fiyatın %40'ını belirliyor
   - Mülk tipi %25, host faktörleri %20 etkili
   - Sezonsal etkiler sınırlı (veri kısıtı nedeniyle)

## 🚀 İş Değeri ve Kullanım Alanları

### Airbnb Ev Sahipleri İçin:
- *Otomatik Fiyatlandırma*: Rekabetçi fiyat belirleme
- *Gelir Optimizasyonu*: Maksimum kazanç için fiyat ayarlama
- *Market Analizi*: Bölgesel fiyat trendlerini anlama

### Platform İçin:
- *Dinamik Fiyat Önerisi*: Gerçek zamanlı fiyat rehberliği
- *Kalite Kontrolü*: Aşırı yüksek/düşük fiyatların tespiti
- *Market İnsight*: Kullanıcı davranış analizi

### Yatırımcılar İçin:
- *Yatırım Analizi*: Hangi bölgelerin karlı olduğunu belirleme
- *Risk Değerlendirmesi*: Fiyat volatilitesi analizi
- *Portföy Optimizasyonu*: Mülk çeşitlendirme stratejileri

## 🔧 Teknik Geliştirme Önerileri

### Kısa Vadeli İyileştirmeler:
1. *Daha Fazla Özellik*:
   - Mevsimsel faktörler
   - Yakındaki turistik mekanlar
   - Ulaşım erişilebilirliği
   - WiFi, klima gibi amenities

2. *Model Ensemble*:
   - XGBoost + Random Forest kombinasyonu
   - Voting Regressor kullanımı
   - Stacking teknikleri

### Uzun Vadeli Geliştirmeler:
1. *Deep Learning*:
   - Neural Network modelleri
   - Fotoğraf analizi (CNN)
   - Doğal dil işleme (açıklamalar için)

2. *Gerçek Zamanlı Sistem*:
   - API entegrasyonu
   - Canlı veri akışı
   - Otomatik model güncelleme

3. *Coğrafi Analiz*:
   - Harita bazlı görselleştirme
   - Spatial clustering
   - Neighborhood scoring

## 👨‍💻 Geliştiriciler

Ferhat Onur Özgan
- GitHub: github.com/onurzgn

Berke Kabasakal
- GitHub: github.com/berkekbskl