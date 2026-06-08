# Mevduat Getiri ve Karşılaştırma Aracı

Bu proje, bankaların "günlük yüksek faiz" adı altında sunduğu ancak anaparanın belirli bir kısmını vadesiz hesapta (boşta) bırakma şartı koşan mevduat ürünlerini, klasik 32 günlük vadeli hesaplarla objektif bir şekilde kıyaslamak için geliştirilmiş yalın ve dinamik bir web aracıdır.

Proje, canlı ortamda test edilmek ve kullanıcıların kendi verileriyle anlık hesaplama yapabilmelerini sağlamak amacıyla tek bir HTML/JS dosyası olarak kurgulanmıştır.

---

## 🚀 Öne Çıkan Özellikler

- **Bileşik Faiz Simülasyonu:** Günlük hesap seçeneğinde, net getiri her gün anaparaya eklenerek 32 günlük bir döngüyle (bileşik olarak) hesaplanır.
- **Gerçekçi Boşta Kalan Tutar Mantığı:** Her gün faiz kazanan ve büyüyen yeni anaparadan, bankanın şart koştuğu "sabit vadesiz tutar" düşülerek net nemalanan tutar dinamik olarak bulunur.
- **Güncel Mevzuat Entegrasyonu:** Hesaplamalarda, yasal kesinti olan güncel **%17,5 stopaj (gelir vergisi) oranı** otomatik olarak uygulanır.
- **Sı

