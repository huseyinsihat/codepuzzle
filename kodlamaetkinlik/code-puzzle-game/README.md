# 🧩 Code Puzzle Game - BİLSEM Python Öğretim Oyunu

> **Interactive Code Sequencing Puzzle Game** | Gamified Python Teaching for BİLSEM Students
> 
> *9-haftalık kümülatif Python eğitimi için etkileşimli bir oyun tabanlı platformu*

![Version](https://img.shields.io/badge/version-1.0-blue) ![React](https://img.shields.io/badge/React-19.2-61dafb) ![Vite](https://img.shields.io/badge/Vite-7.2-64b5f6) ![License](https://img.shields.io/badge/license-MIT-green)

---

## 📋 İçindekiler

- [🎮 Oyun Tanımı](#-oyun-tanımı)
- [✨ Özellikler](#-özellikler)
- [📊 Teknik Mimarı](#-teknik-mimarı)
- [🚀 Kurulum](#-kurulum)
- [🎯 Nasıl Oynanır](#-nasıl-oynanır)
- [📁 Proje Yapısı](#-proje-yapısı)
- [⚙️ Konfigürasyon](#-konfigürasyon)
- [📈 Oyun Özellikleri](#-oyun-özellikleri)
- [🛠️ Geliştirme](#-geliştirme)

---

## 🎮 Oyun Tanımı

**Code Puzzle Game**, BİLSEM (Bilim ve Sanat Merkezleri) öğrencileri için Python programlama dilini öğretmek amacıyla geliştirilmiş, gamifikasyon unsurlarıyla donatılmış bir eğitim oyunudur.

### Temel Konsept

Oyuncular, karmaşık Python kodlarını **parça parça** (fragment) sıralamak zorunda kalırlar. Her haftada yeni konseptler eklenir ve önceki haftalardaki konular kümülatif olarak devam eder.

### Eğitim Hedefleri

- ✅ Python söz dizimi ve yapısını öğrenme
- ✅ Mantıksal düşünmeyi geliştirme
- ✅ Problem çözme becerilerini artırma
- ✅ Kod okuma ve anlama yeteneği kazanma
- ✅ Gamifikasyon ile motivasyon sağlama

---

## ✨ Özellikler

### 🎓 Eğitim Öğeleri

| Özellik | Açıklama |
|---------|----------|
| **9 Hafta Müfredat** | Kümülatif zorluk seviyeleri (Hafta 1 → Hafta 9) |
| **27 Soru** | Hafta başına 3 soru (Hafta 1-9) |
| **9 Boss Sorusu** | Her haftanın son sorusu - 2x puan bonus |
| **Parça Analizi** | Seçilen kodun detaylı açıklaması |
| **Zaman Bonusu** | Hızlı çözüm için ekstra puan (15s=+25, 30s=+10) |

### 🎮 Oyuncu Etkileşimi

| Özellik | Açıklama |
|---------|----------|
| **Tıkla-Seç Sistemi** | Sürükle-bırak yerine basit numara tuşu seçimi (1-6) |
| **Hareket Kontrolleri** | ⬆️ Yukarı, ⬇️ Aşağı, 🗑️ Sil |
| **Canlı Geri Bildirim** | Yanlış sıralama kırmızı renkle gösterilir |
| **Sıralama Alanı** | Seçilen parçaları düzenlemek için |
| **Kod Havuzu** | Tüm kullanılabilir parçalar görünür |

### 🏆 Gamifikasyon

- 🎯 **Skor Sistemi**: Zorluk × zaman bonusu + kombo bonusu
- 🔥 **Kombo**: Art arda doğru cevaplar için bonus
- 🎆 **Kutlama Efektleri**: Doğru cevaplarda konfeti animasyonu
- 📊 **Lider Tablosu**: En yüksek skorlar kaydedilir
- 💾 **LocalStorage**: Oyuncu puanları otomatik kaydedilir

### 📱 Responsive Tasarım

- 📱 **Mobil**: Dikey düzen, tam ekran düğmeler
- 📊 **Tablet**: Yanyana paneller + tam genişlik kod havuzu
- 🖥️ **Masaüstü**: Optimize edilmiş 2-seviye düzen

---

## 📊 Teknik Mimarı

### 🏗️ Stack

```
Frontend:
├── React 19.2          (UI framework)
├── Vite 7.2            (Build tool)
├── Tailwind CSS        (Styling)
├── Framer Motion 12.31 (Animations)
├── canvas-confetti 1.9.4 (Effects)
└── lucide-react        (Icons)

State Management:
└── React Hooks (useState, useEffect)

Storage:
└── Browser LocalStorage (Leaderboard)
```

### 🔄 State Yönetimi

```javascript
// GameScreen.jsx içinde:
- poolOrder[]           // Karıştırılmış soru parçaları
- workspace[]           // Oyuncunun seçtiği parçalar
- selectedPoolId        // Seçili kod havuzu parçası
- selectedWorkspaceIdx  // Sıralama alanında seçili item
- wrongIndices[]        // Yanlış pozisyondaki parçalar
- timer                 // Haftanın sayacı
- playerScore           // Oyuncu puanı
- comboCount            // Art arda doğru cevaplar
```

---

## 🚀 Kurulum

### Ön Gereksinimler

- **Node.js** 16+ 
- **npm** veya **yarn**
- Modern web tarayıcı (Chrome, Firefox, Edge, Safari)

### Adım 1: Repository'yi Klonlayın

```bash
git clone https://github.com/yourusername/code-puzzle-game.git
cd code-puzzle-game
```

### Adım 2: Bağımlılıkları Yükleyin

```bash
npm install
```

### Adım 3: Geliştirme Sunucusunu Başlatın

```bash
npm run dev
```

Tarayıcınızda açın: `http://localhost:5173`

### Adım 4: Production İçin Build Edin

```bash
npm run build
```

Çıktı `dist/` klasöründe yer alır.

---

## 🎯 Nasıl Oynanır

### 1️⃣ Hafta Seçimi
- Hoş geldiniz ekranında 1-9 arasında bir hafta seçin
- Her hafta önceki haftalardaki tüm soruları içerir (kümülatif)

### 2️⃣ Soru Yükleniyor
- **Sıralama Alanı** (SOL): Seçilen parçaları düzenleyeceğiniz yer
- **Parça Analizi** (SAĞ): Seçili parçanın detaylı açıklaması
- **Kod Havuzu** (ALT): Tüm kullanılabilir parçalar (1-6 numaralar)

### 3️⃣ Parça Seçimi
```
KOD HAVUZU:
[1: int(input)]  [2: "Summ"]  [3: puanı]  ...

Yapacağınız:
- [1] tuşuna basın
- [2] tuşuna basın
- [3] tuşuna basın
- ... sıralamayı tamamlayın
```

### 4️⃣ Düzenleme
- ⬆️ **Yukarı**: Seçili parçayı yukarı taşı
- ⬇️ **Aşağı**: Seçili parçayı aşağı taşı
- 🗑️ **Sil**: Seçili parçayı çıkar

### 5️⃣ Doğrulama
- **KONTROL ET** tuşuna basın
- ✅ Doğru: Konfeti efekti + puan kazanın
- ❌ Yanlış: Kırmızı renkli parçalar gösterilir, yeniden deneyin

### 6️⃣ Puan Sistemi

```
Temel Puan:        100 pt
+ Zorluk Bonusu:   × (1-3)
+ Zaman Bonusu:    +25 (≤15s) | +10 (≤30s) | 0 (>30s)
+ Kombo Bonusu:    × (kombo-1) × 15
────────────────────────────────
= Toplam Puan
```

**Boss Soruları**: Haftanın 3. sorusu = 2× puan (isBoss: true)

---

## 📁 Proje Yapısı

```
code-puzzle-game/
├── index.html              # Entry point
├── package.json            # Bağımlılıklar
├── vite.config.js          # Vite konfigürasyonu
├── eslint.config.js        # Linting kuralları
├── README.md               # Bu dosya
│
├── src/
│   ├── main.jsx            # React DOM root
│   ├── index.css           # Global stiller
│   ├── App.css             # App bileşen stilleri
│   ├── App.jsx             # Ana router
│   │
│   ├── components/
│   │   ├── GameScreen.jsx      # 🎮 Ana oyun ekranı (320 satır)
│   │   ├── WelcomeScreen.jsx   # 👋 Hoş geldiniz ve hafta seçimi
│   │   ├── LeaderboardScreen.jsx # 🏆 Lider tablosu
│   │   └── SortableItem.jsx    # (Eski: Drag-drop - kullanımda değil)
│   │
│   ├── data/
│   │   └── questions.json      # 📊 27 soru (1254 satır)
│   │       └── Yapı:
│   │           - id: "w#_q#"
│   │           - week: 1-9
│   │           - topic: Python konsepti
│   │           - title: Soru başlığı
│   │           - timeLimit: Saniye
│   │           - difficulty: 1-3
│   │           - fragments: []  # Parçalar
│   │           - answer: []     # Doğru sıra
│   │           - isBoss: true/false
│   │
│   ├── lib/
│   │   └── utils.js        # Yardımcı fonksiyonlar
│   │
│   └── assets/             # Resimler, fontlar vb.
│
└── dist/                   # Production build (npm run build sonrası)
    ├── index.html
    └── assets/
```

---

## ⚙️ Konfigürasyon

### Build & Development

```bash
# Geliştirme
npm run dev         # http://localhost:5173

# Production
npm run build       # dist/ klasöründe çıktı
npm run preview     # Build'i test et

# Linting
npm run lint        # ESLint kurallarını kontrol et
```

### Tailwind CSS Responsive

```javascript
// Mobile First Breakpoints:
// sm: 640px   | md: 768px  | lg: 1024px | xl: 1280px

// Örnek:
className="w-full md:col-span-8"  // Mobil full, desktop 8/12
```

---

## 📈 Oyun Özellikleri

### Hafta Müfredatı

| Hafta | Konu | Parça | Zorluk |
|-------|------|:---:|:---:|
| 1 | Değişkenler & Giriş | 3 | ⭐ |
| 2 | Veri Tipleri | 3 | ⭐ |
| 3 | Koşullu İfadeler | 3 | ⭐⭐ |
| 4 | Döngüler | 3 | ⭐⭐ |
| 5 | Listeler | 3 | ⭐⭐ |
| 6 | Fonksiyonlar | 3 | ⭐⭐ |
| 7 | Dosya İşlemleri | 3 | ⭐⭐⭐ |
| 8 | Hata Yönetimi | 3 | ⭐⭐⭐ |
| 9 | Kapsamlı Proje | 3 | ⭐⭐⭐ |

### Zorluk Seviyeleri

- 🟢 **Kolay (1)**: Temel konseptler, 20pt bonus
- 🟡 **Orta (2)**: Birleşik konseptler, 40pt bonus  
- 🔴 **Zor (3)**: Gelişmiş konseptler, 60pt bonus

---

## 🛠️ Geliştirme

### Yeni Soru Ekleme

1. `src/data/questions.json` dosyasını açın
2. Aşağıdaki yapıda yeni soru ekleyin:

```json
{
  "id": "w1_q1",
  "week": 1,
  "topic": "Değişkenler",
  "title": "Sayı Girişi",
  "timeLimit": 45,
  "difficulty": 1,
  "fragments": [
    "sayi = ",
    "int(input(",
    "\"Lütfen bir sayı girin: \"",
    "))"
  ],
  "answer": [1, 2, 3, 0],
  "isBoss": false
}
```

### Bileşen Geliştirme

```javascript
// src/components/MyComponent.jsx
import React, { useState } from 'react';
import { ChevronUp } from 'lucide-react';

export default function MyComponent() {
  const [state, setState] = useState(false);
  
  return (
    <div className="p-4 bg-slate-900 rounded-lg">
      {/* Tailwind CSS + React Hooks */}
    </div>
  );
}
```

### Stil Kılavuzu

- **Renkler**: Tailwind dark mode (bg-slate-900 vb.)
- **Responsive**: Mobile-first, md:/lg: breakpoints
- **İkonlar**: lucide-react from 'lucide-react'
- **Animasyonlar**: Framer Motion (motion.div vb.)

---

## 📊 Proje İstatistikleri

- **Toplam Soru**: 27
- **Toplam Parça**: 81
- **Müfredat Haftası**: 9
- **Boss Sorusu**: 9 (Her hafta 1)
- **Zorluk Seviyeleri**: 3
- **Maksimum Puan**: ~5000 (Tamamen optimal çözüm)
- **Build Zamanı**: ~2.2 saniye
- **Bundle Size**: CSS 8KB + JS 365KB (gzip: 2.3KB + 117KB)

---

**Durum**: Production Ready ✅  
**Versiyon**: 1.0  
**Son Güncelleme**: Şubat 2026

---

<div align="center">

Made with ❤️ for BİLSEM Students

⭐ Bu projeyi beğendiyseniz, yıldız vermeyi unutmayın!

</div>
