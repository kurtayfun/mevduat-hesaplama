# Mevduat Getiri ve Karşılaştırma Aracı

Bu proje; bankaların "günlük yüksek faiz" adı altında sunduğu ancak anaparanın belirli bir kısmını vadesiz hesapta (boşta) bırakma şartı koşan mevduat ürünlerini, klasik vadeli hesaplarla objektif bir şekilde kıyaslamak için geliştirilmiş yalın ve dinamik bir web aracıdır.

Kullanıcıların kendi verileriyle anlık ve esnek hesaplama yapabilmelerini sağlamak amacıyla tek bir HTML/JS dosyası olarak kurgulanmıştır.

---

## 🚀 Öne Çıkan Özellikler

- **Dinamik Vade Yönetimi:** Sadece 32 günlük değil; 45, 60, 90 veya dilediğiniz gün sayısındaki vadelerle günlük hesap getirisini çarpıştırabilirsiniz.
- **Bileşik Faiz Simülasyonu:** Günlük hesap seçeneğinde, net getiri her gün anaparaya eklenerek girilen gün süresince bileşik olarak hesaplanır.
- **Gerçekçi Boşta Kalan Tutar Mantığı:** Her gün faiz kazanan ve büyüyen yeni anaparadan, bankanın şart koştuğu "sabit vadesiz tutar" düşülerek net nemalanan tutar dinamik olarak bulunur.
- **Güncel Mevzuat Entegrasyonu:** Hesaplamalarda, yasal kesinti olan güncel **%17,5 stopaj (gelir vergisi) oranı** otomatik olarak uygulanır.
- **Sıfır Bakım ve Operasyonel Kolaylık:** Bankaların sürekli değişen limit tablolarını arka planda takip etmek yerine verilerin kullanıcı tarafından anlık girilmesine imkan tanır. Bu sayede sistem asla eskimez.
- **Mobil Uyumlu ve Temiz Arayüz:** Yenilenen dikey blok tasarımı ve otomatik binlik ayraç desteği sayesinde mobil cihazlarda kusursuz bir veri girişi ve okuma deneyimi sunar.

---

## 🛠️ Kurulum ve Canlıya Alma

Proje tek bir `index.html` dosyasından oluştuğu için herhangi bir sunucu kurulumuna veya bağımlılığa (dependency) ihtiyaç duymaz.

### Yerel Çalıştırma
1. Bu depoda bulunan `index.html` dosyasını bilgisayarınıza indirin.
2. Dosyaya çift tıklayarak herhangi bir modern tarayıcıda (Chrome, Edge, Safari, Firefox) anında çalıştırın.

### GitHub Pages ile Ücretsiz Yayınlama
Aracı internette herkesin erişimine açmak için aşağıdaki adımları takip edebilirsiniz:
1. GitHub üzerinde **Public** bir depo (repository) oluşturun.
2. `index.html` dosyasını deponun ana dizinine (root) yükleyin.
3. Deponun **Settings > Pages** menüsüne gidin.
4. Branch kısmını `main` (veya `master`) olarak seçip **Save** butonuna tıklayın.
5. Birkaç dakika içinde `https://<kullanici-adiniz>.github.io/<depo-adiniz>/` adresinde siteniz yayına girecektir.

---

## 📊 Hesaplama Metodolojisi

### 1. Günlük Hesap (Bileşik)
Kullanıcının girdiği vade gün sayısı boyunca her gün tekrarlanan döngü şu şekildedir:

```text
Net Anapara = Mevcut Anapara - Boşta Kalan Sabit Tutar
Günlük Brüt Getiri = (Net Anapara * Günlük Faiz Oranı) / 36500
Günlük Net Getiri = Günlük Brüt Getiri * (1 - 0.175)
Ertesi Güne Devreden Yeni Anapara = Mevcut Anapara + Günlük Net Getiri
