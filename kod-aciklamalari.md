# 📘 Kod Açıklamaları

Bu dosya `index.html` ve `css/style.css` içindeki her bölümü,
öğrencinin "bu ne işe yarıyor?" sorusuna cevap verecek şekilde açıklar.

---

## 1) `<!DOCTYPE html>` ve `<html lang="tr">`

- `<!DOCTYPE html>` → Tarayıcıya "bu bir HTML5 belgesi" olduğunu söyler.
- `lang="tr"` → Sayfanın Türkçe olduğunu belirtir (ekran okuyucular ve
  arama motorları için önemlidir).

## 2) `<head>` içindeki önemli satırlar

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
Bu satır olmazsa Bootstrap'in **responsive (mobil uyumlu)** özellikleri
çalışmaz! Mobilde sayfanın küçülüp bozulmasını önler.

```html
<link href="...bootstrap.min.css" rel="stylesheet">
```
Bootstrap'in hazır CSS dosyasını internetten (CDN) çekiyoruz.
Bu sayede binlerce satır CSS'i biz yazmadan hazır bileşenleri kullanabiliyoruz.

```html
<link rel="stylesheet" href="css/style.css">
```
**ÖNEMLİ:** Bu satır Bootstrap'ten SONRA gelmeli. Çünkü CSS'te
sonradan yazılan kural, öncekini ezer. Biz Bootstrap'in
bazı stillerini kendi renklerimizle değiştirmek istiyoruz.

## 3) Navbar (üst menü)

Bootstrap'in hazır navbar bileşenini kullanıyoruz:
- `navbar-expand-lg` → geniş ekranda menü yatay, dar ekranda (mobil) hamburger menüye dönüşür
- `data-bs-toggle="collapse"` → JavaScript yazmadan menüyü açıp kapatmayı sağlar (Bootstrap'in kendi JS'i hallediyor)

## 4) Hero (giriş alanı)

`<header class="hero d-flex align-items-center">`
- `hero` → bizim `style.css`'te tanımladığımız özel sınıf (gradient arka plan)
- `d-flex align-items-center` → Bootstrap'in **flexbox** yardımcı sınıfları,
  içeriği dikey ortalar

## 5) Grid Sistemi (row / col)

Bootstrap'in en önemli özelliği: **12 kolonluk grid sistemi**.

```html
<div class="row">
    <div class="col-md-4">...</div>
    <div class="col-md-8">...</div>
</div>
```

- `row` → satır oluşturur
- `col-md-4` → orta ve büyük ekranlarda 12 kolonun 4'ünü kapla (yani 1/3'ünü)
- `col-md-8` → geri kalan 8 kolonu kapla (2/3'ünü)
- `md` → "medium" ve üstü ekranlarda geçerli demek. Mobilde (`md`'den küçükse)
  Bootstrap otomatik olarak kolonları alt alta dizer!

Bu yüzden **hiç medya sorgusu (media query) yazmadan** mobil uyumlu
bir tasarım elde ediyoruz.

## 6) CSS Değişkenleri (`:root`)

```css
:root {
    --renk-vurgu: #ff6b6b;
}
```

`:root` tüm sayfayı kapsayan bir "global" alan gibi düşünülebilir.
İçine tanımladığımız değişkenleri (`--renk-vurgu` gibi) sayfanın
her yerinde `var(--renk-vurgu)` şeklinde kullanabiliriz.

**Neden önemli?** Renk paletini değiştirmek istediğinde tek bir yeri
değiştirmen yeterli olur, kodun içinde renk kodu aramana gerek kalmaz.

## 7) `::after` ile dekoratif çizgi

```css
.section-title::after {
    content: "";
    ...
}
```

`::after`, bir elementin İÇİNE, gerçek HTML yazmadan, CSS ile
"hayali" bir eleman eklemenizi sağlar. Burada başlığın altına
küçük bir çizgi eklemek için kullanılıyor.

## 8) `:hover` ile etkileşim

```css
.project-card:hover {
    transform: translateY(-4px);
}
```

Fare kartın üzerine geldiğinde kartı 4 piksel yukarı kaldırır.
`transition` özelliği bu hareketi ani değil, yumuşak/akıcı yapar.

---

## 9) Genişletilmiş Navbar: Dropdown Menü

```html
<li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">Projeler</a>
    <ul class="dropdown-menu">
        <li><a class="dropdown-item" href="#projeler">Tüm Projeler</a></li>
    </ul>
</li>
```

- `dropdown` sınıfı, bu `<li>`'nin bir açılır menü kapsayıcısı olduğunu belirtir.
- `data-bs-toggle="dropdown"` → tıklanınca menüyü aç/kapat (JavaScript yazmadan!)
- `dropdown-menu` içindeki her `<li>` bir seçenek satırıdır.
- `<hr class="dropdown-divider">` → menüde ince bir ayraç çizgisi ekler.

## 10) Header/Hero: `row` içinde iki kolonlu düzen + istatistik şeridi

Header artık tek bir ortalanmış metin değil, **iki kolonlu** bir yapı:
- `col-lg-7` → sol tarafta tanıtım metni (geniş ekranda 7/12 genişlik)
- `col-lg-5` → sağ tarafta avatar (5/12 genişlik)

`lg` kullandık çünkü mobilde bu iki kolonun yan yana durması okumayı
zorlaştırır — mobilde otomatik olarak alt alta dizilirler.

İstatistik şeridi (`.stats-bar`) basitçe 4 eşit kolon:
```html
<div class="col-6 col-md-3">...</div>
```
`col-6` → mobilde 2'li sıra (12 ÷ 6 = 2)
`col-md-3` → tablet ve üstünde 4'lü sıra (12 ÷ 3 = 4)

## 11) `position: absolute` ile Scroll Göstergesi

```css
.scroll-indicator {
    position: absolute;
    bottom: 1.25rem;
    left: 50%;
    transform: translateX(-50%);
}
```

- `position: absolute` → elemanı normal akıştan çıkarıp, en yakın
  `position: relative` olan üst elemana (burada `.hero`'ya) göre
  konumlandırır. Bu yüzden `.hero`'da `position: relative` tanımlı.
- `left: 50%` + `transform: translateX(-50%)` → bir elemanı YATAY
  olarak tam ortalamanın en yaygın CSS yöntemidir. `left: 50%` elemanın
  SOL kenarını ortaya taşır, `translateX(-50%)` ise elemanın kendi
  genişliğinin yarısı kadar geri çeker — böylece tam ortalanır.

## 12) `@keyframes` ile Basit Animasyon

```css
@keyframes asagi-hareket {
    0%, 100% { transform: translate(-50%, 0); }
    50% { transform: translate(-50%, 8px); }
}
```

`@keyframes` bir animasyonun "hikayesini" tanımlar: başta (0%),
ortada (%50) ve sonda (%100) elemanın nasıl görüneceğini yazarsın.
`animation: asagi-hareket 1.8s ease-in-out infinite;` satırı bu
hikayeyi 1.8 saniyede bir, sonsuza kadar (infinite) tekrar oynatır.

## 13) Genişletilmiş Footer: Çok Kolonlu Düzen

Footer artık 4 kolon: Hakkında, Hızlı Linkler, Teknolojiler, Bülten formu.

```html
<div class="row g-4">
    <div class="col-md-4">...</div>  <!-- Hakkında: geniş -->
    <div class="col-md-2">...</div>  <!-- Hızlı linkler: dar -->
    <div class="col-md-3">...</div>  <!-- Teknolojiler -->
    <div class="col-md-3">...</div>  <!-- Bülten formu -->
</div>
```
4 + 2 + 3 + 3 = 12 ✅ (Bootstrap'te bir satırdaki kolonlar toplamda
12'yi bulmalı, yoksa taşan kolon alt satıra kayar.)

`g-4` → kolonlar arasına boşluk (gap) ekler, "gutter" seviyesi 4.

Footer'daki bülten (newsletter) formu şu an sadece görsel — gerçekten
e-posta göndermiyor, çünkü bunun için JavaScript/backend gerekiyor
(bkz. `bonus/bonus-gorevler.md`).

## 14) Tasarım Token'ları: `:root` Neden Bu Kadar Büyüdü?

Son güncellemede `:root` içine onlarca değişken eklendi: renkler,
fontlar, gölgeler, köşe yuvarlamalar. Buna **design token sistemi**
denir — profesyonel projelerde CSS'in en tepesinde böyle bir
"ayar paneli" bulunur.

```css
:root {
    --accent-orange: #ffa657;
    --golge-md: 0 6px 16px rgba(15, 18, 25, 0.10);
    --radius-md: 14px;
}
```

Neden önemli? Diyelim ki tüm kartların gölgesini biraz daha belirgin
yapmak istiyorsun. Token sistemi olmadan, `box-shadow` yazan HER
satırı tek tek bulup değiştirmen gerekir. Token sistemiyle sadece
`--golge-md` satırını değiştirirsin, tüm sayfa otomatik güncellenir.

## 15) `radial-gradient` ile Atmosferik Arka Plan

```css
background:
    radial-gradient(circle at 15% 20%, rgba(255, 166, 87, 0.10), transparent 40%),
    radial-gradient(circle at 85% 75%, rgba(88, 166, 255, 0.10), transparent 40%),
    var(--bg-dark);
```

CSS'te `background` özelliğine **virgülle ayırarak birden fazla
katman** verebilirsin — en üstteki katman en önce yazılır. Burada
iki soluk, renkli "ışık lekesi" (`radial-gradient`) koyu zeminin
üstüne bindiriliyor. `circle at 15% 20%` → ışığın merkezi, elemanın
soldan %15, yukarıdan %20 noktasında olsun demek. `transparent 40%`
→ ışık, merkezden %40 uzaklıkta tamamen şeffaflaşıp kaybolsun demek.

## 16) `backdrop-filter: blur()` — Camsı (Frosted Glass) Navbar

```css
.navbar {
    background-color: rgba(13, 17, 23, 0.92);
    backdrop-filter: blur(10px);
}
```

`rgba(...)` rengin son değeri (0.92) **yarı saydamlık** demek —
navbar'ın arkası hafifçe görünür. `backdrop-filter: blur(10px)` ise
navbar'ın ARKASINDAKİ içeriği bulanıklaştırır (iOS'taki kontrol
merkezine benzer "buzlu cam" efekti). İkisi birlikte kullanılınca
navbar sabit kaldığında (fixed-top) altından kayan içerik şık bir
şekilde bulanıklaşarak görünür.

## 17) `::after` ile Kayan Alt Çizgi (Navbar Hover Efekti)

```css
.navbar-nav .nav-link::after {
    content: "";
    width: 0;
    height: 2px;
    background-color: var(--accent-orange);
    transition: width 0.25s ease;
}
.navbar-nav .nav-link:hover::after {
    width: 100%;
}
```

Normalde çizginin genişliği (`width`) 0'dır, yani görünmez. Fare
linkin üstüne geldiğinde (`:hover`) genişlik %100 olur. `transition`
sayesinde bu değişim ANİ değil, 0.25 saniyede akıcı şekilde olur.
Bu, "profesyonel" hissi veren en klasik CSS tekniklerinden biridir.

## 18) Erişilebilirlik: `:focus-visible` ve `prefers-reduced-motion`

```css
a:focus-visible {
    outline: 2px solid var(--accent-orange);
}

@media (prefers-reduced-motion: reduce) {
    * { transition-duration: 0.001ms !important; }
}
```

- `:focus-visible` → sadece **klavye ile** (Tab tuşuyla) gezinen
  kullanıcılarda görünen bir çerçeve ekler. Fare tıklamalarında
  görünmez, gereksiz "kutu" oluşturmaz.
- `prefers-reduced-motion` → kullanıcının işletim sisteminde
  "hareketi azalt" ayarı açıksa, tüm animasyonları neredeyse anında
  bitirir. Baş dönmesi gibi rahatsızlık yaşayan kullanıcılar için
  önemli bir incelik.

Gerçek/profesyonel bir site sadece göze hoş görünen değil, **herkesin
kullanabildiği** sitedir. Bu iki kural küçük görünse de, kaliteli
projelerin ayırt edici detaylarındandır.

## 🔑 Bootstrap'i Anlamanın Altın Kuralı

Bootstrap = hazır CSS sınıfları kütüphanesi.
Sen CSS yazmak yerine, doğru **class isimlerini** HTML'e ekliyorsun.

Örnek:
- `mt-3` → margin-top: 1rem (margin top, seviye 3)
- `text-center` → text-align: center
- `d-none` → display: none
- `py-5` → padding üstten ve alttan, seviye 5

Bu kısaltmaları ezberlemene gerek yok, [Bootstrap dokümantasyonuna](https://getbootstrap.com/docs/5.3/utilities/spacing/)
bakarak öğrenebilirsin — gerçek geliştiriciler de sürekli dokümantasyona bakar!
