# 🧩 Code Puzzle Game - BİLSEM Python Oyunu

> Python programlama becerilerini oyun yoluyla öğreten interaktif bir eğitim platformu

[![React](https://img.shields.io/badge/React-19.2-61dafb)](https://react.dev) [![Vite](https://img.shields.io/badge/Vite-7.2-64b5f6)](https://vitejs.dev) [![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 🚀 Hızlı Başlangıç

```bash
# Klonla
git clone https://github.com/huseyinsihat/akissemasi.git
cd code-puzzle-game

# Kur
npm install

# Çalıştır
npm run dev  # http://localhost:5173
```

## 🎮 Nedir?

Oyuncular Python kod parçalarını doğru sırayla yerleştirerek soruları çözerler. 9 haftalık kümülatif müfredat, gamifikasyon sistemi ve lider tablosu ile öğrenmenizi eğlenceli hale getirir.

**27 Soru** | **9 Hafta** | **3 Parça/Soru** | **Responsive Tasarım**

## ✨ Temel Özellikler

| Özellik | Detay |
|---------|-------|
| **Parça Sıralama** | Tıkla-seç sistemi (1-6 numaralar) |
| **Kontroller** | ⬆️ Yukarı, ⬇️ Aşağı, 🗑️ Sil |
| **Puan Sistemi** | Zorluk + Zaman Bonusu + Kombo |
| **Lider Tablosu** | LocalStorage'da otomatik kayıt |
| **Boss Soruları** | Her hafta 3. soru = 2× puan |

## 📊 Teknoloji

```
React 19.2 • Vite 7.2 • Tailwind CSS
Framer Motion • Canvas Confetti • Lucide Icons
```

## 🎯 Kullanım

### 1. Hafta Seçin (1-9)
Her hafta önceki tüm soruları içerir (kümülatif).

### 2. Parçaları Seçin
Kod Havuzundan numaralar tıklayarak sıralamaya ekleyin.

### 3. Düzenleyin
⬆️⬇️ okları ve 🗑️ sil düğmesini kullanın.

### 4. KONTROL ET
✅ Doğru = Puan + Konfeti  
❌ Yanlış = Kırmızı renkli parçalar + Tekrar deneyin

## 📁 Yapı

```
src/
├── components/
│   ├── GameScreen.jsx        # Ana oyun (398 satır)
│   ├── WelcomeScreen.jsx     # Hafta seçimi
│   └── LeaderboardScreen.jsx # Skor tablosu
├── data/
│   ├── questions.json        # 27 soru
│   └── stages.json           # Hafta bilgileri
├── utils/
│   └── highlight.js          # Python syntax highlight
└── App.jsx                   # Router
```

## ⚙️ Komutlar

```bash
npm run dev      # Geliştirme (http://localhost:5173)
npm run build    # Production build
npm run preview  # Build'i test et
npm run lint     # Kod kontrol
```

## 📈 Müfredat (9 Hafta)

| Hafta | Konu | Zorluk |
|-------|------|:---:|
| 1-2 | Değişkenler & Veri Tipleri | ⭐ |
| 3-4 | Koşullar & Döngüler | ⭐⭐ |
| 5-6 | Listeler & Fonksiyonlar | ⭐⭐ |
| 7-9 | Dosya İşlemleri & Hata Yönetimi | ⭐⭐⭐ |

## 💻 Soru Ekleme

`src/data/questions.json` dosyasına ekleyin:

```json
{
  "id": "w1_q1",
  "week": 1,
  "topic": "Değişkenler",
  "title": "Sayı Girişi",
  "timeLimit": 45,
  "difficulty": 1,
  "fragments": ["sayi = ", "int(input(", "\"Lütfen: \"", "))"],
  "answer": [1, 2, 3, 0],
  "isBoss": false
}
```

## 📊 İstatistikler

- **Toplam Soru**: 27
- **Kod Parçası**: 81
- **Boss Sorusu**: 9 (her hafta 1)
- **Build Zamanı**: ~2.2s
- **Bundle**: CSS 8KB + JS 365KB (gzip)

## 📱 Responsive

- 📱 Mobil: Dikey düzen
- 📊 Tablet: Yanyana + Full-width
- 🖥️ Desktop: Optimize edilmiş layout

---

**Versiyon**: 1.0 | **Durum**: Production Ready ✅

<div align="center">

Made with ❤️ for BİLSEM Students

⭐ Beğendin mi? Yıldız ver!

</div>
