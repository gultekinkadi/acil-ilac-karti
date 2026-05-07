# Acil İlaç Kartı 2025

Acil serviste sık kullanılan ilaçların doz ve uygulama bilgilerini kategorize eden, tek dosyadan oluşan web uygulaması.

> **Hazırlayan:** GK / MAA — 2025

---

## 📋 İçerik

| Kategori | İlaç Sayısı |
|---|---|
| Resüsitasyon İlaçları | 21 |
| Hızlı Seri Ardışık Entübasyon (RSI) | 10 |
| Antikonvülzanlar | 4 |
| Ajitasyon Tedavisi | 3 |
| Antidotlar ve Endikasyonları | 17 |

**RSI kategorisi** kendi içinde alt bölümlere ayrılmıştır: ön tedavi (hipotansiyon), sedatifler (etki başlangıcı + süre) ve paralizanlar.

---

## 🚀 Kullanım

### Direkt açmak için

Dosyayı indirip tarayıcıda açın:

```
acil_ilac_karti_2025.html → Çift tıkla → Tarayıcıda açılır
```

### GitHub Pages ile yayınlamak için

1. Bu repoyu fork'layın ya da klonlayın
2. GitHub repo ayarlarından **Settings → Pages** bölümüne gidin
3. Source olarak `main` branch ve `/ (root)` seçin
4. Kaydedin — birkaç dakika içinde şu adreste yayına girer:

```
https://<kullanıcı-adı>.github.io/acil-ilac-karti/acil_ilac_karti_2025.html
```

---

## ⚙️ Teknik Detaylar

- **Tek dosya:** Tüm uygulama `acil_ilac_karti_2025.html` içinde — framework, build adımı ya da sunucu gerekmez
- **Bağımlılıklar (CDN):** Tabler Icons, IBM Plex Sans / Mono (Google Fonts) — internet bağlantısı gerekir
- **Sıfır JavaScript framework:** Vanilla JS, ~150 satır
- **Arama:** Tüm kategorilerde ilaç adı, doz ve endikasyon üzerinden anlık filtreleme
- **Responsive:** Mobil ekranlarda sidebar gizlenir

---

## ⚠️ Uyarı

Bu uygulama **yalnızca hızlı referans** amaçlıdır. Klinik karar verme süreçlerinde güncel kılavuzlar, hastane protokolleri ve uzman görüşü esas alınmalıdır. Dozlar hastaya, kliniğe ve yerel protokollere göre farklılık gösterebilir.

---

## 📁 Dosya Yapısı

```
acil-ilac-karti/
└── acil_ilac_karti_2025.html   # Uygulamanın tamamı
└── README.md                   # Bu dosya
```

---

## 🔄 Güncelleme

İlaç eklemek veya mevcut dozu değiştirmek için `acil_ilac_karti_2025.html` içindeki `TABS` dizisini düzenleyin. Her ilaç şu yapıdadır:

```js
{
  name: "İlaç Adı",
  b: "b-teal",           // renk: b-red, b-blue, b-amber, b-purple, b-teal, b-gray
  doses: [
    "Doz bilgisi 1",
    "Doz bilgisi 2"
  ],
  route: "IV"            // uygulama yolu
}
```

Antidot kategorisinde `route` yerine `endik` (endikasyon) alanı kullanılır.
