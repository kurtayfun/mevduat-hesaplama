---

## 📊 Hesaplama Metodolojisi

### 1. Günlük Hesap (Bileşik)
Kullanıcının girdiği vade gün sayısı boyunca her gün tekrarlanan döngü şu şekildedir:
- Net Anapara = Mevcut Anapara - Boşta Kalan Sabit Tutar
- Günlük Brüt Getiri = (Net Anapara * Günlük Faiz Oranı) / 36500
- Günlük Net Getiri = Günlük Brüt Getiri * (1 - 0.175)
- Ertesi Güne Devreden Yeni Anapara = Mevcut Anapara + Günlük Net Getiri

### 2. Klasik Vadeli Hesap
Vade sonunda tek seferde hesaplanır:
- Toplam Brüt Getiri = (Toplam Anapara * Düz Vade Oranı * Girilen Gün Sayısı) / 36500
- Toplam Net Getiri = Toplam Brüt Getiri * (1 - 0.175)

---

