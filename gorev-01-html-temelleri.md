# 📝 Görev 1 — HTML Temelleri

**Amaç:** `index.html` dosyasını okuyup anlamak ve kendi bilgilerinle
kişiselleştirmek.

## Yapılacaklar

1. [ ] `index.html` dosyasını aç ve tüm bölümleri sırayla oku
       (Navbar → Hero → Hakkımda → Yetenekler → Projeler → İletişim → Footer).
2. [ ] "Ahmet Yılmaz" yazan tüm yerleri kendi adınla değiştir
       (title etiketi, hero başlığı, footer).
3. [ ] "Hakkımda" bölümündeki metni kendi hikayenle yeniden yaz
       (en az 3 cümle).
4. [ ] "Yetenekler" bölümüne, gerçekten bildiğin veya öğrenmek
       istediğin bir teknoloji daha ekle (örnek: Git, Figma).
       İpucu: mevcut `<div class="col-6 col-md-3">` bloklarından
       birini kopyala.
5. [ ] "İletişim" bölümündeki `mailto:` linkini kendi (gerçek veya
       hayali) e-posta adresinle değiştir.
6. [ ] Footer'daki telif hakkı satırını kontrol et, yılı doğru mu?

## Kontrol Soruları

Bu görevi bitirdikten sonra kendine şu soruları sor:

- `<section>` ile `<div>` arasındaki fark nedir? Neden bazı yerlerde
  `<section>`, bazı yerlerde `<div>` kullanılmış?
<!--  <section> etiketinin anlamsal semantik bir anlam taşıması div etiketinin ise hiçbir anlamı olmayan genel bir gruplayıcı olması -->
- `id="hakkimda"` gibi id'ler ne işe yarıyor? (İpucu: navbar'daki
  linklere bak: `href="#hakkimda"`)
  <!--  Belirli bir öğreti css ile şekillendirmek javascript ile seçip yönetmek veya sayfa içi bağlantılarla o noktaya doğrudan gitmek için kullanılır -->
- Bir `<a>` etiketinin `href` özelliği neden önemlidir?
<!--  HTML <a> (bağlantı) etiketindeki href özelliği, kullanıcının bir bağlantıya tıkladığında gideceği hedef adresin (URL) veya kaynağın yerini belirler. -->

## Bitirme Kriteri

Sayfanı tarayıcıda açtığında:
- Kendi adın ve bilgilerin görünüyor olmalı
- Navbar'daki menü linklerine tıklayınca ilgili bölüme gitmeli
- Hiçbir yerde "Ahmet Yılmaz" veya örnek metin kalmamalı
