# 📊 DBSCAN Kümeleme Analizi: Iris ve Wine Veri Setleri Üzerinde

Bu proje, **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algoritmasının farklı `eps` ve `min_samples` parametre kombinasyonlarıyla **Iris** ve **Wine** veri setleri üzerinde nasıl çalıştığını ve kümeleri nasıl etkilediğini görselleştirmektedir.

---

## 📁 İçerik

- [Kullanılan Veri Setleri](#kullanılan-veri-setleri)
- [Uygulanan Yöntem](#uygulanan-yöntem)
- [Parametre Kombinasyonları](#parametre-kombinasyonları)
- [Sonuçların Görselleştirilmesi](#sonuçların-görselleştirilmesi)
- [Kurulum ve Kullanım](#kurulum-ve-kullanım)
- [Bağımlılıklar](#bağımlılıklar)

---

## 📊 Kullanılan Veri Setleri

1. **Iris Veri Seti**  
   - Yalnızca ilk iki özellik (sepal length ve sepal width) kullanılmıştır.
   - Kümeleme işlemi 2 boyutlu uzayda gerçekleştirilmiştir.

2. **Wine Veri Seti**  
   - Tüm özellikler kullanılmış, ardından boyut indirgeme için **PCA (Principal Component Analysis)** uygulanarak 2 bileşene indirgenmiştir.
   - Kümeleme, bu 2 bileşenli uzayda yapılmıştır.

---

## 🧠 Uygulanan Yöntem

- Veriler `StandardScaler` ile ölçeklendirilmiştir.
- Her veri seti için aşağıdaki `eps` ve `min_samples` değer kombinasyonlarıyla **DBSCAN** uygulanmıştır.
- Her kombinasyon için çıktı kümeleri 2D uzayda görselleştirilmiştir.
- Gürültü (noise) noktaları siyah renkle gösterilmiştir.

---

## ⚙️ Parametre Kombinasyonları

DBSCAN parametreleri şu şekilde denenmiştir:

| eps  | min_samples |
|------|-------------|
| 0.3  | 5           |
| 0.3  | 10          |
| 0.5  | 5           |
| 0.5  | 10          |
| 0.8  | 5           |
| 0.27 | 10          |

---

## 📈 Sonuçların Görselleştirilmesi

### Iris Veri Seti (2 Özellik)

- Her bir parametre kombinasyonu için kümeler ayrı subplot'larda gösterilmiştir.
- Kümeler farklı renklerle, `-1` etiketiyle gösterilen gürültü verileri ise siyah ile gösterilir.

### Wine Veri Seti (PCA Sonrası)

- PCA ile 2 bileşene indirgenmiş veri üzerinde DBSCAN kümeleme yapılmıştır.
- Aynı parametre kombinasyonları burada da kullanılmıştır.

---

## 🚀 Kurulum ve Kullanım

1. Gerekli kütüphaneleri yükleyin:
```bash
pip install numpy matplotlib scikit-learn
