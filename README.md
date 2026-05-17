# Random Forest ile Spor Salonu Yoğunluk Tahmini 

Bu depo, bir spor salonundaki kişi sayısını çeşitli zamansal ve çevresel özelliklere dayanarak tahmin eden bir makine öğrenmesi projesidir. Model, günün saati, sıcaklık ve akademik takvim gibi faktörlerin spor salonu doluluğunu nasıl etkilediğini analiz etmek için **Random Forest Regressor** kullanılarak oluşturulmuştur.

##  Proje Özeti
Spor salonu yoğunluğunu anlamak, tesis yönetimi ve antrenman programlarını optimize etmek için oldukça önemlidir. Bu projede, `15-gym_crowdedness.csv` veri setini analiz ettim, EDA yaptım ve belirli bir zamanda salonda bulunacak kesin kişi sayısını tahmin etmek için bir Random Forest modeli eğittim.

##  Temel Özellikler
* **EDA:** Spor salonu katılımcılarının dağılımını görselleştirme ve özellikler arası korelasyonları inceleme.
* **Feature Engineering:** timestamp ile anlamlı zamansal özellikler çıkarma ve tarih-saat dönüşümlerini işleme.
* **Regresyon Modellemesi:** Random Forest Regressor modelinin kurulması ve eğitilmesi.
* **Performans Metrikleri:** Modeli hem eğitim hem de test veri setlerinde değerlendirmek için RMSE, MAE ve R² Skoru hesaplamaları.

##  Veri Seti Bilgileri
Veri seti, aşağıdaki temel özellikleri içeren `62.184` kayıttan oluşmaktadır:
- `number_people`: Hedef değişken (anlık kişi sayısı)
- `day_of_week`, `is_weekend`, `is_holiday`: Zamansal ve tatil göstergeleri
- `temperature`: sıcaklık
- `is_start_of_semester`, `is_during_semester`: Akademik takvim dönemi durumu
- `month`, `hour`, `year`: Zaman damgasından türetilmiş özellikler

##  Kullanılan Teknolojiler ve Kütüphaneler
- **Python 3.x**
- **Pandas & NumPy** 
- **Matplotlib & Seaborn** 
- **Scikit-Learn** 

##  Model Değerlendirmes
Projede, modelin aşırı öğrenmeye (overfitting) düşmeden veriyi iyi genellediğinden emin olmak için hem Eğitim hem de Test setleri üzerinde aşağıdaki metrikler hesaplanmıştır:
* **RMSE:** 6.42
* **MAE:** 4.29
* **R² Skoru:** 0.92
