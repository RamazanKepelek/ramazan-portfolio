# 🚀 Bonus Görevler

Ana görevleri bitiren ve daha fazlasını denemek isteyen öğrenciler için.
Zorluk sırasına göre dizilmiştir.

## 🟢 Kolay

1. **Google Fonts entegrasyonu**
   [fonts.google.com](https://fonts.google.com) üzerinden bir font seç,
   `<head>` içine `<link>` ekle ve `style.css`'te `font-family`'yi
   güncelle.

2. **Favicon ekle**
   Tarayıcı sekmesinde görünen küçük ikonu (favicon) ekle:
   ```html
   <link rel="icon" href="favicon.ico">
   ```

3. **Karanlık mod renk paleti**
   `:root` içine ikinci bir renk seti daha ekleyip, mevcut renklerin
   koyu tema versiyonlarını hazırla (henüz aktif etmeden, sadece
   renkleri tanımla).

## 🟡 Orta

4. **Scroll ile görünme animasyonu (Bootstrap + basit CSS)**
   `section-title` elemanlarına, sayfa kaydırıldığında yumuşakça
   belirme efekti eklemeyi araştır (İpucu: CSS `transition` ve
   `opacity` kullanılabilir, veya `IntersectionObserver` JS API'si
   — bu JavaScript öğrendikten sonra daha kolay olacak).

5. **İletişim formu ekle**
   Bootstrap'in form bileşenlerini kullanarak (isim, e-posta, mesaj)
   alanları olan bir form ekle. Dokümantasyon: Components → Forms.
   Not: Form şimdilik gerçekten mesaj göndermeyecek, bunun için
   JavaScript/backend gerekecek — bu ileride öğrenilecek.

6. **Aktif menü linki vurgusu**
   Kullanıcı hangi bölümdeyse (Hakkımda, Yetenekler, vb.) navbar'daki
   ilgili linkin farklı renkte görünmesini sağla. (İpucu: Bu tam
   otomatik yapmak JavaScript gerektirir — şimdilik `:target` CSS
   seçicisini araştırabilirsin.)

## 🔴 Zor (JavaScript / React'e geçiş öncesi ısınma)

7. **Karanlık mod butonu**
   Sağ üst köşeye tıklanınca temayı karanlık/açık arasında
   değiştiren bir buton ekle. Bu, JavaScript dersine geçtiğinde
   yapılacak — şimdiden HTML/CSS tarafını (buton, ikon, renk
   değişkenleri) hazırlayabilirsin.

8. **Proje kartlarını dinamikleştir**
   Şu an her proje kartı elle yazılmış HTML. İleride JavaScript
   öğrendiğinde, projelerini bir liste (array) halinde tutup
   otomatik olarak kart oluşturmayı deneyeceksin. Şimdiden şu soruyu
   düşün: "Bu 3 kartın HTML'i neden neredeyse birebir aynı? Bu
   tekrarı nasıl azaltırdım?"

9. **React'e hazırlık sorusu**
   Bu portfolyoyu ileride React ile yeniden yapacaksın. Şimdiden
   şunu düşün: Navbar, Hero, Hakkımda, Yetenekler, Projeler,
   İletişim, Footer — bunların her biri ayrı bir "bileşen (component)"
   olsaydı, kodun nasıl daha düzenli olurdu?

---

💡 **Not:** Bonus görevlerin hepsini yapmak zorunda değilsin. Amaç
merak ettiğin konuyu seçip derinleşmek.
