<div align="center">

# 🔴 YunalCore — External CS2 Hile Sistemi

### En Güvenli Undetected External Counter-Strike 2 Hilesi — Salt-Okunur Bellek Mimarisi

[![Website](https://img.shields.io/badge/Website-yunalcore.app-d90429?style=for-the-badge&logo=google-chrome&logoColor=white)](https://yunalcore.app)
[![Durum](https://img.shields.io/badge/Durum-UNDETECTED-22c55e?style=for-the-badge&logo=checkmarx&logoColor=white)](https://yunalcore.app)
[![Yöntem](https://img.shields.io/badge/Yöntem-EXTERNAL%20(RPM)-blue?style=for-the-badge&logo=shield&logoColor=white)](https://yunalcore.app)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://yunalcore.app)

<br/>

<img src="https://yunalcore.app/img/esp.png" alt="YunalCore CS2 ESP Overlay Ekran Görüntüsü" width="720"/>

<br/>

**YunalCore**, Counter-Strike 2 için geliştirilmiş %100 undetected **external** hile sistemidir. Internal hilelerden farklı olarak, oyun sürecine hiçbir şekilde müdahale etmez — yalnızca **salt-okunur bellek erişimi** (ReadProcessMemory) kullanır. Bu sayede **oyun verisi hiçbir zaman değiştirilmez**, enjeksiyon riski sıfırdır ve **değerli hesaplarınız için en yüksek güvenlik seviyesi** sağlanır.

[🌐 Web Sitesi](https://yunalcore.app) · [📥 Kayıt Ol](https://yunalcore.app/register) · [💬 Destek](https://yunalcore.app/help)

</div>

---

## 🛡️ Neden External, Internal'dan Daha Güvenli?

CS2 hilesi seçerken anlamanız gereken en önemli konu budur. Kullanılan yöntem, hesabınızın güvenliğini doğrudan belirler:

### ❌ Internal Hileler (Riskli)
Internal hileler, **cs2.exe sürecine DLL enjekte ederek** ve **oyun belleğine doğrudan veri yazarak** (WriteProcessMemory) çalışır. Bu demektir ki:
- Oyun verilerini **değiştirirler** — VAC, değiştirilmiş bellek bölgelerini tespit edebilir
- DLL enjeksiyonu, süreç handle tablosunda **adli iz** bırakır
- **Hook** (fonksiyon yönlendirme) kullanırlar — VAC bunları aktif olarak tarar
- Oyun bütünlük kontrolleri değiştirilmiş kod bölümlerini algılayabilir
- **Sonuç: Yüksek ban riski**, özellikle skinli ve yüksek rankli değerli hesaplarda

### ✅ YunalCore External (Güvenli)
YunalCore, oyun sürecinin **tamamen dışında** çalışır:
- Yalnızca **ReadProcessMemory** kullanır — oyun belleği **asla değiştirilmez**
- **DLL enjeksiyonu yok** — cs2.exe'ye hiçbir şey yüklenmez
- **Hook yok** — fonksiyon yönlendirme yok, IAT yaması yok
- **Sürücü (driver) yok** — anti-cheat uyarısı tetikleyecek kernel bileşeni yok
- **Ayrı overlay penceresi** üzerinde render yapar — oyun kendisi dokunulmaz
- **Sonuç: Premium hesaplar, ranked oyun ve uzun vadeli güvenlik için tasarlanmıştır**

```
┌──────────────────────────────────────────────────────────────┐
│                   INTERNAL vs EXTERNAL                       │
├────────────────────────────┬─────────────────────────────────┤
│   ❌ Internal Hile         │   ✅ YunalCore (External)       │
├────────────────────────────┼─────────────────────────────────┤
│ Oyuna DLL enjekte eder     │ Ayrı .exe olarak çalışır       │
│ WriteProcessMemory kullanır│ Sadece ReadProcessMemory        │
│ Oyun fonksiyonlarını hooklar│ Sıfır hook, sıfır yönlendirme │
│ Oyun verisini değiştirir   │ Oyun verisi asla dokunulmaz     │
│ Enjeksiyon izi bırakır     │ Adli iz bırakmaz               │
│ Kernel sürücü gerektirir   │ Sürücü gerektirmez              │
│ Yüksek VAC algılama riski  │ %100 VAC undetected             │
│ Ana hesaplar için riskli   │ Premium hesaplar için güvenli   │
└────────────────────────────┴─────────────────────────────────┘
```

> **Özet:** Değerli skinleri, madalyaları veya yüksek rankı olan bir Steam hesabınız varsa — internal hile kullanmak hesabınızla kumar oynamaktır. YunalCore'un external mimarisi, **hesabını kaybetme lüksü olmayan kullanıcılar** için özel olarak tasarlanmıştır.

---

## ⚡ Özellikler

### 🎯 İnsansılaştırılmış Aimbot
- Dinamik yumuşatma eğrileriyle **çok noktalı kemik hedefleme**
- Bağımsız **Geri Tepme Kontrol Sistemi (RCS)** — spray paternlerini yok eder
- Silaha özel yapılandırılabilir FOV, hız ve kemik önceliklendirme
- Profesyonel oyuncu nişanını taklit eden insansılaştırılmış fare hareketi
- Görüş kontrolü — asla duvardan ateş etmez

### 👁️ Overlay ESP (Ekstra Duyusal Algı)
- **Kutu ESP** — 2D / 3D / Köşe sınır kutuları
- **İskelet ESP** — Gerçek zamanlı kemik yapısı çizimi
- **Sağlık çubukları** — Renk kodlu sağlık göstergeleri
- **İsim & Mesafe** — Oyuncu bilgi katmanı
- **Silah ikonları** — Her düşmanın hangi silahı taşıdığını görün
- **Bağlantı çizgileri** — Düşman pozisyonlarına yön çizgileri
- Tamamen özelleştirilebilir renkler, kalınlık ve çizim mesafesi

### 🔫 Triggerbot
- Nişangâh hedefe hizalandığında otomatik ateş
- İnsansı tepki için yapılandırılabilir **gecikme süresi** (min/max ms)
- Kemiğe özel tetikleme (sadece kafa, gövde veya tümü)
- Sıfır gecikme için **ayrı thread** üzerinde çalışır

### 🔐 Çok Katmanlı Güvenlik Mimarisi
| Katman | Teknoloji | Amacı |
|--------|----------|-------|
| **Mimari** | %100 External (RPM) | Oyuna müdahale yok, enjeksiyon yok |
| **Binary** | Polimorfik build'ler | Her kullanıcıya benzersiz çalıştırılabilir dosya |
| **String'ler** | XorStr şifreleme | Tüm metin içerikleri derleme zamanında şifreli |
| **API Çağrıları** | LazyImporter | WinAPI çağrıları IAT'den gizli |
| **Lisanslama** | HWID Kilidi | Donanıma bağlı, 30 günlük otomatik sıfırlama |
| **Anti-Cheat** | VAC Bypass | Kanıtlanmış %100 koruma |

### ☁️ Bulut Altyapısı
- **Otomatik Offset Güncelleyici** — CS2 yamaları sonrası dakikalar içinde uyum sağlar
- **Bulut Silah Ayarları** — Silaha özel ayarları kaydet, yükle ve paylaş
- **Durum Paneli** — Abonelik, HWID ve sistem sağlığını takip et

### 🎨 Ek Özellikler
- **Radar Hack** — Düşman pozisyonlarıyla geliştirilmiş minimap
- **Bomba Sayacı** — Hassas C4 geri sayım overlay'ı
- **Seyirci Uyarısı** — Birinin sizi izlediğini bilin
- **Özel Nişangâh** — Yapılandırılabilir overlay nişangâhı
- **Gece Modu** — Tam ekran renk filtresi (overlay tabanlı, belleğe yazma yok)

---

## 🖥️ Sistem Gereksinimleri

| Bileşen | Minimum | Önerilen |
|---------|---------|----------|
| **İşletim Sistemi** | Windows 10 64-bit | Windows 11 64-bit |
| **İşlemci** | Intel i5 / AMD Ryzen 5 | Intel i7 / AMD Ryzen 7 |
| **RAM** | 8 GB | 16 GB |
| **GPU** | DirectX 11 uyumlu | — |

> **Ek yazılım, sürücü veya kernel modülü gerekmez.** YunalCore bağımsız bir external uygulama olarak çalışır.

---

## 📦 Hızlı Başlangıç

```
1. Hesap Oluştur    →  yunalcore.app'de kayıt ol
2. Plan Seç         →  Abonelik seç (7 günlük — Ömür Boyu)
3. İndir            →  Sana özel polimorfik build'ini al
4. HWID Bağla       →  Tek tıkla donanım kaydı
5. Başlat & Oyna    →  CS2'yi aç ve hükmetmeye başla
```

### Nasıl Çalışır

```
┌──────────────────────────────────────────────┐
│              YunalCore Client                │
│                                              │
│  ┌─────────┐  ┌─────────┐  ┌──────────────┐ │
│  │ Aimbot  │  │   ESP   │  │  Triggerbot  │ │
│  │ Motoru  │  │ Overlay │  │   (Thread)   │ │
│  └────┬────┘  └────┬────┘  └──────┬───────┘ │
│       │            │              │          │
│  ┌────┴────────────┴──────────────┴───────┐  │
│  │    Bellek Okuyucu (RPM — Salt Okunur)  │  │
│  │  Enjeksiyon Yok · Hook Yok · Yazma Yok │  │
│  └────────────────┬───────────────────────┘  │
│                   │                          │
│  ┌────────────────┴───────────────────────┐  │
│  │     Bulut Offset Güncelleyici Servisi  │  │
│  │   CS2 yamalarından sonra otomatik uyum │  │
│  └────────────────────────────────────────┘  │
└──────────────────────────────────────────────┘
                    │
         ReadProcessMemory (Salt Okunur)
                    │
          ┌─────────┴─────────┐
          │   CS2 (cs2.exe)   │
          │  ⚠️ ASLA DEĞİŞMEZ │
          └───────────────────┘
```

---

## 💰 Fiyatlandırma

| Plan | Süre | Fiyat |
|------|------|-------|
| **Başlangıç** | 7 Gün | ₺49.99 |
| **Standart** | 30 Gün | ₺149.99 |
| **Premium** | 90 Gün | ₺349.99 |
| **Ömür Boyu** | Sınırsız | ₺2,499.99 |

Tüm planlar şunları içerir:
- ✅ %100 VAC Ban Koruması
- ✅ Hesap Güvenlik Garantisi
- ✅ Polimorfik Build (Benzersiz .exe)
- ✅ Otomatik Güncelleme & Bulut Offset'ler
- ✅ 7/24 Destek Bileti
- ✅ Bulut Silah Ayarları

---

## ❓ Sıkça Sorulan Sorular

<details>
<summary><strong>Ana hesabım için gerçekten güvenli mi?</strong></summary>
<br/>
Evet. YunalCore %100 external'dir — yalnızca oyun belleğini okur, asla değiştirmez. DLL enjeksiyonu yok, hook yok, sürücü yok. CS2 hileleri için mevcut en güvenli yöntemdir. Kullanıcılarımızın büyük çoğunluğu pahalı envanterleri ve yüksek ranklı hesaplarda kullanmaktadır.
</details>

<details>
<summary><strong>External ve internal hile arasındaki fark nedir?</strong></summary>
<br/>
Internal hileler, oyuna doğrudan kod (DLL) enjekte eder ve oyun belleğine veri yazar. Bu, VAC tarafından kolayca tespit edilebilir. YunalCore gibi external hileler ayrı bir süreç olarak çalışır ve sadece oyun belleğini OKUR — oyunun kendisine asla dokunulmaz. Bu nedenle external hilelerin algılanma riski temelden çok daha düşüktür.
</details>

<details>
<summary><strong>HWID kilidimi sıfırlayabilir miyim?</strong></summary>
<br/>
Evet, donanıma bağlı lisansınız otomasyon sistemi üzerinden her 30 günde bir sıfırlanabilir. Bilgisayar veya parça değişikliği sorun yaratmaz.
</details>

<details>
<summary><strong>CS2 güncellemelerinden sonra çalışmaya devam eder mi?</strong></summary>
<br/>
Offset güncelleyici sistemimiz, CS2'ye yeni bir yama geldiğinde bulut sunucuları üzerinden dakikalar içinde otomatik uyum sağlar. Kesintisiz kullanım — manuel güncelleme gerekmez.
</details>

<details>
<summary><strong>Competitive/Premier modunda kullanmak güvenli mi?</strong></summary>
<br/>
YunalCore'un insansılaştırılmış aimbot'u ve external mimarisi, Premier ve Competitive dahil tüm oyun modları için uygundur. Yumuşatma eğrileri ve tepki gecikmeleri, oyununuzu doğal gösterir.
</details>

<details>
<summary><strong>Seçkin/değerli hesabımda kullanabilir miyim?</strong></summary>
<br/>
Kesinlikle. YunalCore'un external mimarisi tam olarak bu amaç için tasarlanmıştır. Oyun belleğine hiçbir veri yazılmadığı, DLL enjeksiyonu yapılmadığı ve hook kullanılmadığı için, skinli, madalyalı ve yüksek ranklı hesaplarda güvenle kullanılabilir. Internal hileler oyuna doğrudan müdahale ettiği için her zaman risk taşır — external mimarimiz bu riski sıfıra indirir.
</details>

---

## 📸 Ekran Görüntüleri

| Aimbot Ayarları | Triggerbot Ayarları | Config Yöneticisi |
|:---:|:---:|:---:|
| ![Aimbot](https://yunalcore.app/img/aimbot1.png) | ![Triggerbot](https://yunalcore.app/img/triggerbot.png) | ![Config](https://yunalcore.app/img/config.png) |

| ESP Overlay 1 | ESP Overlay 2 | ESP Overlay 3 |
|:---:|:---:|:---:|
| ![ESP](https://yunalcore.app/img/esp.png) | ![ESP2](https://yunalcore.app/img/esp2.png) | ![ESP3](https://yunalcore.app/img/esp3.png) |

| Tema Özelleştirme |
|:---:|
| ![Tema Seçenekleri](https://yunalcore.app/img/theme.png) |

---

## 🔗 Bağlantılar

| Kaynak | URL |
|--------|-----|
| 🌐 **Resmi Web Sitesi** | [yunalcore.app](https://yunalcore.app) |
| 📥 **Kayıt Ol** | [yunalcore.app/register](https://yunalcore.app/register) |
| 🔐 **Giriş Yap** | [yunalcore.app/login](https://yunalcore.app/login) |
| 📋 **Yasal Politikalar** | [yunalcore.app/legal](https://yunalcore.app/legal) |
| 💬 **Destek Merkezi** | [yunalcore.app/help](https://yunalcore.app/help) |

---

## ⚠️ Sorumluluk Reddi

YunalCore, **eğitim amaçları, güvenlik araştırması ve oyun test otomasyonu** için geliştirilmiştir. Çevrimiçi rekabetçi ortamlarda kullanımı, oyunun hizmet koşullarını ihlal edebilir. Geliştiriciler, kötüye kullanımdan kaynaklanan sonuçlardan sorumlu değildir. Riski kabul ederek kullanınız.

---

<div align="center">

**© 2026 YunalCore Systems. Tüm Hakları Saklıdır.**

[![Website](https://img.shields.io/badge/🌐_Ziyaret_Et-yunalcore.app-d90429?style=flat-square)](https://yunalcore.app)

</div>
