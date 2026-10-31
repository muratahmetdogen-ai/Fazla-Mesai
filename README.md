# Mesai Takip

Telefonda kişisel kullanım için hazırlanmış, internet olmadan da çalışabilen bir PWA uygulamasıdır. Uygulamada ücret veya maaş hesabı yapılmaz; yalnızca çalışma, fazla mesai, eksik mesai ve izin saatleri takip edilir.

## Varsayılan çalışma programı

- Mesai başlangıcı: **07:45**
- Mesai bitişi: **17:45**
- Günlük Hedef: **9 saat**
- Cumartesi ve Pazar hafta tatilidir.
- 1 Ocak 2025 öncesi molalar: **10:00–10:10** ve **12:15–13:05**
- 1 Ocak 2025 sonrası molalar: **10:00–10:10**, **12:15–12:55** ve **15:30–15:40**
- Akşam yemek molası: **17:45–18:15**. Fazla mesai 18:15'ten sonra başlar.
- Sabahlama çalışmasında **02:00–02:40** gece molası düşülür.

Çalışma ve mola saatleri Ayarlar bölümünden değiştirilebilir. Yeni program seçilen tarihten itibaren kullanılır; daha önce kaydedilmiş günler değişmez.

## Temel kullanım

- **Bugün normal çalışma yapıldı:** Günün normal mesai saatlerini kaydeder.
- **Fazla mesai yapıldı:** Normal mesainin üzerine ek çalışma yazmak için kayıt ekranını açar.
- **Bugünü düzenle:** Bugünkü kaydı değiştirir.
- **Geçmiş Kayıt Ekle:** Geçmiş bir tarih için kayıt oluşturur.
- Takvimden eski bir güne dokunarak o günü düzenleyebilir veya yeni kayıt ekleyebilirsiniz.
- Her güne not, fotoğraf veya belge eklenebilir.

Uygulamada canlı kronometre yoktur. Çalışma kaydı için giriş ve çıkış saati yazılır.

## Fazla ve eksik mesai

Fazla mesai değerleri yeşil ve **+** ile, eksik mesai değerleri kırmızı ve **−** ile gösterilir. Fazla mesai daha sonra saatlik izin olarak kullanılabilir: **1 saat fazla mesai = 1 saat izin**.

Varsayılan olarak fazla mesailer ay içinde kullanılmalıdır. Ayın son 14 gününde yapılan fazla mesailer, sonraki ayın 7. gününe kadar kullanılabilir. Bu süreler Ayarlar bölümünden değiştirilebilir.

## İzinler

- Saatlik İzin
- Yıllık İzin
- Şirket / Zorunlu İzin
- Sağlık Raporu
- Resmi Tatil
- Sabahlama Sonrası Dinlenme

Yıllık izin toplamı Ayarlar bölümünden yazılır; kullanılan izinler kalan izinden otomatik düşer. Sabahlama sonrası dinlenme günü yıllık izinden ve fazla mesaiden düşmez.

## Birden çok iş yeri

Uygulama tek bir firmaya bağlı değildir. Birden çok iş yeri eklenebilir. Her iş yerinin kayıtları, çalışma saatleri, yıllık izni ve fazla/eksik mesai toplamı ayrı tutulur.

## Rapor ve yedek

- Aylık, yıllık ve toplam fazla/eksik mesai istatistikleri
- Excel (CSV) raporu
- PDF / yazdırma
- CSV dosyasıyla geçmiş kayıtları toplu aktarma
- Yedek indirip geri yükleme
- Verileri, raporları, fotoğraf ve belgeleri GitHub ile eşitleme

Fotoğraf ve belge dosyalarının kendisi JSON yedeğine eklenmez; GitHub eşitlemesiyle saklanabilir.

## Veri ve gizlilik

Kayıtlar telefonunuzda tutulur. GitHub eşitlemesinde yalnızca depo adı ve erişim anahtarı girilir; veriler kendi özel GitHub deponuza kaydedilir. GitHub erişim anahtarınız yalnızca cihazınızda saklanır; anahtarınızı kimseyle veya sohbetle paylaşmayın.

Şifre kilidi, uygulamanın başka kişiler tarafından açılmasını zorlaştırır ancak verileri şifrelemez.

## Telefona kurulum

Uygulamayı kalıcı olarak kullanmak için dosyaları HTTPS adresinde yayınlayın ve telefonda açın:

- **Android (Chrome):** Menü → **Uygulamayı yükle / Ana ekrana ekle**
- **iPhone (Safari):** Paylaş → **Ana Ekrana Ekle**

## Dosyalar

- `index.html` — Uygulamanın tamamı
- `manifest.webmanifest` — Telefona kurulum bilgileri
- `sw.js` — İnternetsiz çalışma
- `icon-192.png`, `icon-512.png` — Uygulama simgeleri

## Resmi tatiller

Ulusal bayramlar her yıl otomatik eklenir. Dini bayram ve arife günleri 2025–2026 için tanımlıdır. Başka yıllar için ilgili gün takvimden **Resmi Tatil** olarak işaretlenebilir.
