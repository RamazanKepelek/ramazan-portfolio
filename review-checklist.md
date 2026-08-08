# ✅ Code Review Checklist

Öğrenci görevleri bitirdikten sonra, öğretmen (veya öğrencinin kendisi)
bu listeyi kullanarak kodu gözden geçirir. Amaç hata avlamak değil,
**iyi alışkanlıklar kazandırmak**.

## 🧱 HTML

- [ ] Her açılan etiket düzgün kapatılmış mı? (`<div>` ... `</div>`)
- [ ] `<img>` etiketleri varsa `alt` özelliği eklenmiş mi?
      (Görme engelli kullanıcılar ve SEO için önemli)
- [ ] Başlık hiyerarşisi mantıklı mı? (Sayfada tek bir `<h1>`,
      altında `<h2>`'ler, gerekirse `<h3>`'ler — atlama yapılmamalı)
- [ ] Anlamsal (semantic) etiketler doğru kullanılmış mı?
      (`<section>`, `<header>`, `<footer>` — her şey `<div>` olmamalı)
- [ ] Kod girintili (indented) ve okunabilir mi?

## 🎨 CSS

- [ ] Renkler `:root` içindeki değişkenlerden mi geliyor, yoksa
      her yerde farklı renk kodu mu yazılmış? (Tutarlılık önemli)
- [ ] Yazı ve arka plan rengi arasında yeterli kontrast var mı?
      (Okunabilirlik testi: gözünü kısıp bak, hâlâ okuyabiliyor musun?)
- [ ] Gereksiz tekrar eden CSS kuralları var mı?
- [ ] `!important` kullanılmış mı? (Başlangıç seviyesinde kaçınılması
      öğretilmeli — genelde bir CSS seçici sorununu gizler)

## 🅱️ Bootstrap Kullanımı

- [ ] Grid sistemi (`row`/`col-*`) doğru kullanılmış mı?
      (Bir satırdaki kolonların toplamı 12'yi geçmemeli)
- [ ] Gereksiz yere özel CSS yazılmış mı, oysa hazır bir Bootstrap
      utility class'ı (örnek: `mt-3`, `text-center`) o işi zaten
      yapabilirdi?
- [ ] Responsive (mobil uyumlu) davranış test edilmiş mi?

## 📱 Genel Kalite

- [ ] Sayfa farklı ekran boyutlarında (telefon, tablet, masaüstü)
      test edildi mi?
- [ ] Tarayıcı konsolunda (F12) hata var mı?
- [ ] Tüm linkler çalışıyor mu? (Navbar menüsü, footer, iletişim linki)
- [ ] Sayfa başlığı (`<title>`) anlamlı mı, hâlâ "Ahmet Yılmaz" mı
      yazıyor yoksa öğrenci kendi ismini mi yazdı?

## 💬 Geri Bildirim Şablonu

Öğretmen bu bölümü doldurarak öğrenciye geri bildirim verebilir:

```
👍 İyi yapılanlar:
-

🔧 Geliştirilmesi gerekenler:
-

🎯 Bir sonraki hedef:
-
```
