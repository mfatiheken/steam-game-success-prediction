# Steam Oyun Başarısının Tahmini

## 1. Proje Hakkında

Steam'de her yıl çok sayıda oyun yayınlanıyor ancak bazı oyunlar daha fazla oyuncuya ulaşırken bazıları daha az ilgi görüyor. Bu projede oyunların fiyatı, türü, çıkış tarihi ve kullanıcı değerlendirmeleri gibi özelliklerin oyun başarısıyla ilişkisini incelemek istiyorum.

**Araştırma sorusu:** Steam oyunlarının özellikleri ve kullanıcı değerlendirmeleri kullanılarak bir oyunun başarılı olup olmadığı tahmin edilebilir mi?

**Projenin amacı:** Steam oyunlarına ait verileri inceleyerek oyun başarısıyla ilişkili özellikleri belirlemek ve bu özelliklerden yararlanarak bir tahmin modeli geliştirmek.

## 2. Ön Literatür

Proje için Steam oyunlarının popülerliği, başarı tahmini ve kullanıcı yorumları üzerine üç akademik çalışma belirledim.

1. **De Luisa ve arkadaşları (2021)** – *Predicting the Popularity of Games on Steam*. Bu çalışmada oyunların fiyatı, türü ve diğer özellikleri ile popülerlikleri arasındaki ilişki incelenmiştir. [Makaleyi incele](https://arxiv.org/abs/2110.02896)

2. **Guzsvinecz ve Szűcs (2023)** – *Length and sentiment analysis of reviews about top-level video game genres on the Steam platform*. Bu çalışmada Steam'deki milyonlarca kullanıcı yorumu incelenerek oyun türleri ve yorumlardaki duygu özellikleri araştırılmıştır. [Makaleyi incele](https://doi.org/10.1016/j.chb.2023.107955)

3. **Preedanon ve Kluaymai-ngarm (2026)** – *Predicting the Success of Games on Steam Platform*. Bu çalışmada Steam oyunlarının başarı durumunu tahmin etmek için lojistik regresyon kullanılmıştır. [Makaleyi incele](https://so06.tci-thaijo.org/index.php/TNIJournalBA/article/view/290220)

Bu kaynaklar, oyun özellikleri ve kullanıcı değerlendirmelerinin oyun başarısını araştırırken incelenebilecek değişkenler olduğunu göstermektedir.

## 3. Veri Seti

**Veri setinin adı:** Steam Games Dataset 2025

**Kaynak:** Kaggle

**Bağlantı:** https://www.kaggle.com/datasets/artermiloff/steam-games-dataset

**Lisans:** Kaggle sayfasında MIT License olarak belirtilmiştir.

Veri seti, Mart 2025 itibarıyla Steam'de yayınlanan 90.000'den fazla oyuna ait bilgileri içermektedir.

İncelenmesi planlanan değişkenler şunlardır:

- Oyun fiyatı
- Oyun türü ve etiketleri
- Çıkış tarihi
- Kullanıcı değerlendirmeleri
- Olumlu ve olumsuz yorum sayıları, veri setinde mevcutsa
- Tahmini sahip sayısı veya oyuncu sayısı gibi başarı göstergeleri, mevcut sütunlara bağlı olarak

Veri setini seçmemin nedeni, çok sayıda oyuna ait bilgileri bir arada sunması ve araştırma sorusunu incelemek için uygun bir başlangıç noktası olmasıdır. Analiz öncesinde sütunlar, eksik veriler ve lisans koşulları kontrol edilecektir.

## 4. İlk Yöntem ve Hipotez

Bu çalışmada nicel araştırma yaklaşımı kullanılacak ve hazır bir veri seti üzerinden ikincil veri analizi yapılacaktır.

İlk aşamada **Lojistik Regresyon** algoritmasının kullanılması planlanmaktadır. Oyunlar, belirlenecek başarı ölçütüne göre başarılı ve başarısız şeklinde iki gruba ayrılacaktır. Başarı ölçütü, veri setindeki uygun değişkenler ve dağılımlar incelendikten sonra kesinleştirilecektir.

**Hipotez (H1):** Kullanıcı değerlendirme oranı ve toplam yorum sayısı yükseldikçe bir oyunun belirlenen başarı ölçütünü karşılama olasılığının artması beklenmektedir.

Modelin sonuçları doğruluk, precision, recall ve F1-score gibi ölçütlerle değerlendirilecektir.

## 5. Gelecek Adımlar

1. Veri setini indirmek ve sütunlarını incelemek.
2. Eksik veya hatalı verileri kontrol etmek.
3. Oyun başarısını ölçmek için uygun bir değişken ve eşik belirlemek.
4. Verileri modelleme için hazırlamak.
5. Lojistik Regresyon modelini uygulamak.
6. Model sonuçlarını değerlendirmek ve hipotezi incelemek.
7. Elde edilen sonuçları ve çalışmanın sınırlılıklarını raporlamak.

## 6. Kaynakça

De Luisa, A., Hartman, J., Nabergoj, D., Pahor, S., Rus, M., Stevanoski, B., Demšar, J., & Štrumbelj, E. (2021). *Predicting the popularity of games on Steam*. Elektrotehniški vestnik, 88(4), 151–162. https://arxiv.org/abs/2110.02896

Guzsvinecz, T., & Szűcs, J. (2023). *Length and sentiment analysis of reviews about top-level video game genres on the Steam platform*. Computers in Human Behavior, 149, 107955. https://doi.org/10.1016/j.chb.2023.107955

Preedanon, D., & Kluaymai-ngarm, J. (2026). *Predicting the success of games on Steam platform*. Journal of Business Administration and Languages, 14(2), 56–75. https://so06.tci-thaijo.org/index.php/TNIJournalBA/article/view/290220
