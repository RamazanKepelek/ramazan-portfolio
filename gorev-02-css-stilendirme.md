# 📝 Görev 2 — CSS ile Stilendirme

**Amaç:** `css/style.css` dosyasını değiştirerek sayfayı kendi
zevkine göre kişiselleştirmek.

## Yapılacaklar

1. [ ] `:root` içindeki renkleri değiştir:
   - `--renk-koyu`
   - `--renk-vurgu`
   - `--renk-acik-bg`

   İpucu: [coolors.co](https://coolors.co) gibi bir siteden kendine
   3-4 renkli bir palet seç.

2. [ ] `.hero` bölümündeki `background` (gradient) rengini yeni
       renklerinle uyumlu hale getir.

3. [ ] `font-family` değerini değiştirerek farklı bir yazı tipi dene
       (örnek: `"Trebuchet MS"`, `"Verdana"`, veya Google Fonts'tan
       bir font ekleyip onu kullan — bonus görevlerde detaylı anlatılıyor).

4. [ ] `.skill-card:hover` içindeki `transform` değerini değiştirerek
       hover efektini kendi zevkine göre ayarla (örnek: `scale(1.05)`
       dene).

5. [ ] Kendi eklediğin bir CSS kuralı yaz: `.section-title`'a
       `letter-spacing` ekleyerek harfler arası boşluğu artır.

## Kontrol Soruları

- `var(--renk-vurgu)` yazdığında tarayıcı ne yapıyor?
- var() CSS’te daha önce tanımlanmış olan değişkeni çağırır ve değerini kullanır.
- `:hover` ne zaman devreye giriyor?
-:hover, fare bir HTML öğesinin üzerine geldiğinde o öğeye tanımlanan CSS kurallarını devreye sokar.
- `.section-title::after` satırını silersen ne olur? Dene ve gözlemle.
-section-title::after kuralı mevcut CSS dosyasında bulunmadığı için silindiğinde görsel bir değişiklik olmadı.
- `margin` ile `padding` arasındaki fark nedir? (`docs/kod-aciklamalari.md`'de
margin elementin dışında padding içeriğin ve border arasında
  ipucu var, ama kendi cümlenle açıklamaya çalış.)

## Bitirme Kriteri

- Sayfa artık "Ahmet'in şablonu" gibi değil, **senin** tasarımın gibi
  görünmeli.
- En az 3 renk değeri değişmiş olmalı.
- Sayfa hâlâ okunabilir olmalı (yazı-arka plan kontrastına dikkat et!).
