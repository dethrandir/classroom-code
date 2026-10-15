# Classroom Code

Küçük ders alıştırmaları için sade, çalışan ve derste kullanılan yöntemlere uygun kod ile ayrı bir çalışma notu üreten agent talimatı.

## Kullanım

Agent'ın dosya okuyabildiği bir ortamda şu isteği ver:

```text
Bu görev için classroom-code/SKILL.md dosyasını oku ve uygula.

Görev: ...
Derste gösterilen konular / örnek kod: ...
Kullanılmaması gerekenler: ...
```

Dosyanın yolunu bulunduğu konuma göre değiştir. Dosya okuma olanağı yoksa SKILL.md içeriğini görevle birlikte talimata ekleyebilirsin. Bu yöntem belirli bir agent'ın yerleşik skill keşfine bağlı değildir. Otomatik keşif ve kurulum konumları kullanılan ürüne göre ayrıca ayarlanır.

Yalnızca görev tanımı da yeterli olabilir. Konu listesini veya hocanın örnek kodunu eklemek, agent'ın henüz gösterilmeyen yöntemleri seçmesini önlemeye yardımcı olur. Agent bu bilgileri kendiliğinden bilemez.

## Örnek

```text
Bu görev için classroom-code/SKILL.md dosyasını oku ve uygula.

Java Swing ile iki sayı alan, dört işlem yapan basit hesap makinesi.
Derste JFrame, JPanel, JButton, JTextField, JLabel, temel layout'lar,
if/else ve anonim ActionListener gösterildi.
Lambda veya ek kütüphane kullanma. Yorum satırı ve ek özellik ekleme.
Mevcut projenin dosya düzenini koru.
```

## Varsayılanlar

- Gereken davranışı sağlayan basit çözüm.
- Yorum satırı, ek özellik ve gereksiz katman yok.
- Verilen ders örneklerinin yöntem ve tarzına uyum.
- Bilerek hata eklemeden çalışan kod ve kısa sonuç mesajı.
- Koddan ayrı bir Markdown dosyasında çözüme özel açıklamalar ve soru-cevaplar.

Ödevin açık gereksinimleri bu varsayılanlardan önce gelir. Her dersin konu sınırı kendi isteğinde belirlenir.

## Çalışma notları

Agent, varsayılan olarak görev çalışma alanında `study-notes/<alistirma-adi>.md` oluşturur. Dosya kaynak kod klasörlerinin dışında tutulur. Başka bir konum belirtebilir veya o görev için not oluşturulmamasını isteyebilirsin. Notlar konuşmanın dilinde hazırlanır; aynı alıştırma güncellendiğinde ilgili not da güncellenir.

Notlarda programın mantığı, önemli fonksiyon ve değişkenlerin görevleri, kullanılan yaklaşımın nedeni ve hocanın sorabileceği çözüme özel soruların kısa cevapları bulunur. Bir örnek girdinin adım adım nasıl işlendiği, denemek için küçük bir değişiklik, çalıştırma bilgisi ve gerçekten yapılan kontroller de açıklanır. İçerik alıştırmanın büyüklüğüne göre kısa tutulur ve üretilen kodla eşleşir.

Bu özellik belirli bir dil veya derse bağlı değildir. Örneğin bir arayüz alıştırmasında butona basılınca ne olduğu; bir algoritma alıştırmasında döngünün, koşulların ve değişkenlerin nasıl ilerlediği açıklanır. Dosya yazamayan bir ortamda agent notları koddan ayrı bir bölüm olarak sunar ve dosya kaydedilmediğini belirtir.
