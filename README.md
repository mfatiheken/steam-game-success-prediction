# Steam Oyunlarının Başarısını Tahmin Etme

## 1. Proje Hakkında

Bu projede Steam platformundaki oyunların özelliklerine ve kullanıcı değerlendirmelerine bakarak oyunların başarılı olup olmadığını tahmin etmeye çalışacağım.

Steam'de çok fazla oyun bulunuyor ve her oyun aynı başarıyı elde edemiyor. Oyunların fiyatı, türü ve kullanıcı yorumları gibi özelliklerin başarıyla ilişkili olup olmadığını araştırmak istiyorum.

**Araştırma sorum:** Bir oyunun özelliklerine ve kullanıcı değerlendirmelerine bakarak başarılı olup olmayacağını tahmin edebilir miyiz?

## 2. Daha Önce Yapılan Araştırmalar

Projeye başlamadan önce konuyla ilgili bazı akademik çalışmaları inceledim.

- **Predicting the Popularity of Games on Steam (2021):** Bu çalışmada Steam oyunlarının popülerliğinin oyun özelliklerinden yararlanılarak tahmin edilmesi araştırılmıştır.

  https://arxiv.org/abs/2110.02896

- **Length and sentiment analysis of reviews about top-level video game genres on the Steam platform (2023):** Bu araştırmada Steam kullanıcı yorumları incelenmiş ve oyun türlerine göre yorumların özellikleri analiz edilmiştir.

  https://doi.org/10.1016/j.chb.2023.107955

- **Predicting the Success of Games on Steam Platform (2026):** Bu çalışmada Steam oyunlarının başarısını tahmin etmek için farklı oyun özellikleri ve lojistik regresyon yöntemi ele alınmıştır.

  https://so06.tci-thaijo.org/index.php/TNIJournalBA/article/view/290220

## 3. Kullanacağım Veri Seti

Projede Kaggle üzerinden paylaşılan **Steam Games Dataset 2025** veri setini kullanmayı planlıyorum.

**Veri seti bağlantısı:**

https://www.kaggle.com/datasets/artermiloff/steam-games-dataset

İlk olarak veri setini indirip içindeki bilgileri inceleyeceğim. Veri setinde bulunması durumunda oyunların fiyatı, türü, çıkış tarihi, kullanıcı yorumları ve olumlu-olumsuz değerlendirme sayıları gibi bilgileri kullanacağım.

Ayrıca hangi sütunların mevcut olduğunu, eksik verilerin bulunup bulunmadığını ve veri setinin kullanım koşullarını kontrol edeceğim.

## 4. Kullanacağım Yöntem

Bu projede sayısal veriler üzerinden ilerleyeceğim. İlk olarak veri setini inceleyip gerekli düzenlemeleri yapacağım.

Daha sonra **Lojistik Regresyon** yöntemini kullanarak oyunları başarılı ve başarılı olmayan şeklinde sınıflandırmayı deneyeceğim. Bunun için öncelikle bir oyunun hangi koşullarda başarılı sayılacağını belirlemem gerekiyor.

Modelin sonuçlarını değerlendirmek için doğruluk (accuracy), kesinlik (precision), duyarlılık (recall) ve F1 skoru gibi ölçütleri kullanmayı planlıyorum.

**Araştırma beklentim:** Olumlu kullanıcı yorumlarının ve yorum sayısının oyunların başarısıyla ilişkili olabileceğini düşünüyorum. Analiz sonucunda bu beklentinin verilerle desteklenip desteklenmediğini inceleyeceğim.

## 5. Projede İzleyeceğim Adımlar

1. Veri setini indirip incelemek.
2. Kullanabileceğim sütunları belirlemek.
3. Eksik veya hatalı verileri kontrol edip gerekli düzenlemeleri yapmak.
4. Oyunun başarısını belirlemek için uygun bir ölçüt seçmek.
5. Lojistik Regresyon modelini oluşturmak.
6. Modelin sonuçlarını değerlendirmek.
7. Elde ettiğim sonuçları yorumlayıp proje raporunu hazırlamak.

## 6. Kaynakça

1. De Luisa, A. ve diğerleri (2021). *Predicting the Popularity of Games on Steam*. Elektrotehniški vestnik, 88(4), 151–162.

   https://arxiv.org/abs/2110.02896

2. Guzsvinecz, T. ve Szűcs, J. (2023). *Length and sentiment analysis of reviews about top-level video game genres on the Steam platform*. Computers in Human Behavior, 149, 107955.

   https://doi.org/10.1016/j.chb.2023.107955

3. Preedanon, D. ve Kluaymai-ngarm, J. (2026). *Predicting the Success of Games on Steam Platform*. Journal of Business Administration and Languages, 14(2), 56–75.

   https://so06.tci-thaijo.org/index.php/TNIJournalBA/article/view/290220

4. Artermiloff. *Steam Games Dataset 2025*. Kaggle.

   https://www.kaggle.com/datasets/artermiloff/steam-games-dataset

   ## UML Diyagramları

Bu bölümde projenin planlanan yapısını göstermek için üç UML diyagramı hazırlanmıştır.

### 1. Use Case Diagram
Araştırmacının veri setini yükleme, inceleme ve temizleme, modeli eğitme, tahmin yapma ve sonuçları görüntüleme işlemlerini gösterir.

![Use Case Diagram](diagrams/use_case_diagram.png)

### 2. Activity Diagram
Veri setinin incelenmesinden modelin eğitilmesine ve sonuçların değerlendirilmesine kadar planlanan iş akışını gösterir.

![Activity Diagram](diagrams/activity_diagram.png)

### 3. Class Diagram
Dataset, Game, DataPreprocessor, DataSplit, PredictionModel, Evaluation ve PredictionResult sınıflarını ve aralarındaki ilişkileri gösterir.

![Class Diagram](diagrams/class_diagram.png)
