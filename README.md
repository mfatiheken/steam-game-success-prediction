# Steam Oyun Başarısının Tahmini

## Problem ve Amaç

Steam'de çok fazla oyun yayınlanıyor ancak bu oyunların hepsi aynı başarıyı elde edemiyor. Bazı oyunlar çok fazla oyuncuya ulaşırken bazıları çok az oyuncu tarafından oynanıyor. Oyunların fiyatı, türü, kullanıcı yorumları ve çıkış tarihi gibi özelliklerin bu başarıda etkili olabileceğini düşünüyorum. Bu projede bu özellikleri inceleyerek bir oyunun başarılı olup olmayacağını tahmin etmeye çalışacağım.

**Araştırma sorusu:** Steam oyunlarının özellikleri ve kullanıcı değerlendirmeleri kullanılarak bir oyunun başarılı olup olmadığı tahmin edilebilir mi?

## Ön Literatür ve Kaynaklar

| Kaynak | Çalışmanın amacı | Kullanılan yöntem/veri | Projeme katkısı |
| Preedanon & Kluaymai-ngarm (2026) | Steam oyunlarının başarısını etkileyen faktörleri araştırmak | 47.557 oyun ve lojistik regresyon | Steam oyunlarının başarı durumunun tahmin edilebileceğini gösteriyor. |
| Ma (2025) | Oyunların başarısı ve gelirini etkileyen faktörleri incelemek | Steam, Twitch ve Metacritic verileri | Oyuncu sayısı ve yorum sayısı gibi değerlerin başarı için önemli olabileceğini gösteriyor. |
| Guzsvinecz & Szűcs (2023) | Steam kullanıcı yorumlarını incelemek | Steam kullanıcı yorumları | Kullanıcı yorumlarının oyunlar hakkında anlamlı bilgi sağlayabileceğini gösteriyor. |

### Kaynakça

1. Preedanon, D., & Kluaymai-ngarm, J. (2026). *Predicting the success of games on Steam platform*. Journal of Business Administration and Languages, 14(2), 56–75.

2. Ma, J. (2025). *Unveiling success drivers in gaming: A machine learning study across Steam, Twitch, and Metacritic*. International Journal of Computer Games Technology, 2025, Article 5776632.

3. Guzsvinecz, T., & Szűcs, J. (2023). *Length and sentiment analysis of reviews about top-level video game genres on the Steam platform*. Computers in Human Behavior, 149, 107955.

## Veri Seti

**Veri seti:** Steam Games Dataset 2025

**Kaynak:** Kaggle

**Bağlantı:**  
https://www.kaggle.com/datasets/artermiloff/steam-games-dataset

**Lisans:** MIT License

Veri setinde 90.000'den fazla Steam oyunu bulunmaktadır.

Projede kullanmayı düşündüğüm bazı veriler:

- Oyun fiyatı
- Oyun türü
- Çıkış tarihi
- Olumlu yorum sayısı
- Olumsuz yorum sayısı
- Toplam yorum sayısı
- Oyunun tahmini sahip sayısı
- En yüksek eşzamanlı oyuncu sayısı

Bu veri setini seçmemin nedeni hem oyunların özelliklerini hem de kullanıcı değerlendirmelerini aynı veri setinde bulundurmasıdır.

## İlk Yöntem ve Hipotez

Bu projede sayısal veriler kullanılacağı için nicel bir çalışma yapılacaktır. Hazır bir Steam veri seti kullanılacak ve veriler üzerinde analiz yapılacaktır.

İlk olarak Lojistik Regresyon yöntemini kullanmayı düşünüyorum. Bunun nedeni oyunları başarılı ve başarısız olmak üzere iki gruba ayırarak tahmin yapmaya uygun olmasıdır.

**Hipotez:** Kullanıcı değerlendirmesi daha yüksek olan ve daha fazla yorum alan oyunların başarılı olma ihtimalinin daha yüksek olacağı düşünülmektedir.

Başlangıçta oyunun tahmini sahip sayısını başarı ölçütü olarak kullanmayı düşünüyorum. 100.000 ve üzeri tahmini sahip sayısına sahip oyunlar başarılı, altında kalan oyunlar başarısız olarak değerlendirilecektir. Veri seti incelendikten sonra bu değer değiştirilebilir.

## Gelecek Adımlar

1. Veri setini indirmek.
2. Verileri incelemek ve eksik verileri temizlemek.
3. Kullanılacak değişkenleri belirlemek.
4. Oyunları başarılı ve başarısız olarak sınıflandırmak.
5. Lojistik Regresyon modelini uygulamak.
6. Modelin sonuçlarını incelemek.
7. Gerekirse yöntemi veya kullanılan değişkenleri değiştirmek.
