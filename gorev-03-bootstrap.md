# 📝 Görev 3 — Bootstrap ile Genişletme

**Amaç:** Bootstrap'in hazır bileşenlerini keşfedip sayfaya yeni
özellikler eklemek.

Bootstrap dokümantasyonu: https://getbootstrap.com/docs/5.3/components/

## Yapılacaklar

1. [ ] **Badge (Rozet) ekle:** "Projeler" bölümündeki her kart başlığının
       yanına bir Bootstrap badge ekle (örnek: "Yeni", "Tamamlandı").
       Dokümantasyon: Components → Badge

2. [ ] **Alert (Uyarı kutusu) ekle:** "İletişim" bölümünün üstüne,
       "Mesajınıza 24 saat içinde dönüş yapıyorum 📩" yazan bir
       Bootstrap alert kutusu ekle.
       Dokümantasyon: Components → Alerts

3. [ ] **Progress bar ekle:** "Yetenekler" bölümüne, her teknoloji için
       yüzde olarak ne kadar bildiğini gösteren bir progress bar ekle.
       Dokümantasyon: Components → Progress

4. [ ] **Yeni bir kolon düzeni dene:** "Projeler" bölümünü şu an
       `col-md-4` kullanıyor (3'lü sıra). Bunu `col-md-6` yaparak
       2'li sıraya çevir ve farkı gözlemle.

5. [ ] **Responsive test:** Tarayıcıda F12'ye basıp "mobil görünüm"
       moduna geç. Menü hamburger ikonuna dönüşüyor mu? Kartlar
       alt alta diziliyor mu?

## Kontrol Soruları

- Bootstrap bileşenlerini eklerken neden `class="..."` dışında
  bir şey yazmana gerek kalmadı?
- `col-md-4` yerine `col-md-6` yapınca kartlar neden 2'li sıraya geçti?
  (İpucu: 12 ÷ 6 = ?)
- Bootstrap kullanmadan bu bileşenleri (badge, alert, progress bar)
  kendi CSS'inle yapman gerekseydi, kaç satır kod yazman gerekirdi
  sence?

## Bitirme Kriteri

- En az 2 yeni Bootstrap bileşeni sayfaya eklenmiş olmalı.
- Sayfa mobilde test edilmiş ve düzgün görünüyor olmalı.
- Konsol'da (F12 → Console) hiç kırmızı hata olmamalı.
