# Mesai Takip

Telefonda kişisel kullanım için hazırlanmış, internet olmadan da çalışabilen bir PWA uygulamasıdır. Mesai bölümünde ücret hesabı yapılmaz; çalışma, fazla mesai, eksik mesai ve izin saatleri takip edilir. Ayrı **Maaş** menüsünde manuel maaş, vergi iadesi ve yan hak kayıtları tutulur.

## Varsayılan çalışma programı

- Mesai başlangıcı: **07:45**
- Mesai bitişi: **17:45**
- Günlük Hedef: **9 saat**
- Cumartesi ve Pazar hafta tatilidir.
- Hafta sonu çalışılırsa program **08:00–16:30**; molalar **10:00–10:10**, **12:30–13:10** ve **15:00–15:10** olur. Net çalışmanın tamamı fazla mesai sayılır. Çalışma sürerse **16:30–17:00** akşam yemek molası düşülür ve 17:00 sonrası süre fazla mesaiye eklenir.
- 1 Ocak 2025 öncesi hafta içi molaları: **10:00–10:10** ve **12:15–13:05**
- 1 Ocak 2025 sonrası hafta içi molaları: **10:00–10:10**, **12:15–12:55** ve **15:30–15:40**
- Hafta içi akşam yemek molası: **17:45–18:15**. Fazla mesai 18:15'ten sonra başlar.
- Sabahlama çalışmasında **02:00–02:40** gece molası düşülür.

Hafta içi ve hafta sonu çalışma/mola saatleri Ayarlar bölümünde ayrı ayrı değiştirilebilir. Gün kaydı, tarihe göre ilgili programı otomatik kullanır; ayrı bir hafta sonu kayıt kartı gerekmez. Yeni program seçilen tarihten itibaren kullanılır; daha önce kaydedilmiş günler değişmez.

## Temel kullanım

- **Bugün için kayıt gir:** Bugünün gün kayıt ekranını doğrudan açar.
- **Geçmiş Kayıt:** Üst bölümden geçmiş bir tarih için kayıt ekranını açar.
- Takvimden eski bir güne dokunarak o günü düzenleyebilir veya yeni kayıt ekleyebilirsiniz.
- Her güne not, fotoğraf veya belge eklenebilir.

### Gün içinde birden fazla işlem

Bir gün tek giriş/çıkıştan oluşmak zorunda değildir. Güne dokununca **Gün İçindeki İşlemler** altında o günkü aralıklar alt alta gösterilir. **+ Çalışma Ekle** ve **+ Saatlik İzin Ekle** düğmeleriyle yeni aralık eklenebilir.

Örnek:

- **07:45–11:15 Çalışma**
- **11:15–15:00 Saatlik İzin**
- **15:00–21:45 Çalışma**

Sabit program molaları çalışma aralıklarından otomatik düşülür. Saatlik İzin aralığında da program içindeki mola süresi izin kullanımına sayılmaz. Yukarıdaki örnekte net çalışma **9 saat 25 dakika**, kullanılan saatlik izin **3 saat 5 dakika**, kazanılan fazla mesai **25 dakika** olur. Birbiriyle çakışan aralıklar kaydedilemez. Eski tek giriş/çıkış kayıtları açıldığında otomatik olarak tek Çalışma aralığına dönüştürülür.

Uygulamada canlı kronometre yoktur. Her işlem için başlangıç ve bitiş saati yazılır.

## Fazla ve eksik mesai

Fazla mesai değerleri yeşil ve **+** ile, eksik mesai değerleri kırmızı ve **−** ile gösterilir. Fazla mesai daha sonra saatlik izin olarak kullanılabilir: **1 saat fazla mesai = 1 saat izin**.

Varsayılan olarak fazla mesailer ay içinde kullanılmalıdır. Ayın son 14 gününde yapılan fazla mesailer, sonraki ayın 7. gününe kadar kullanılabilir. Bu süreler Ayarlar bölümünden değiştirilebilir.

## İzinler

- Saatlik İzin
- Yıllık İzin
- Sağlık Raporu
- Resmi Tatil
- Sabahlama Sonrası Dinlenme

Her iş yeri için işe başlama tarihi girilebilir. Uygulama firmada kaç gündür çalıştığınızı ve yeni yıllık iznin ekleneceği tarihe kaç gün kaldığını gösterir. İzin dönemleri işe başlama tarihinin yıl dönümlerine göre listelenir; önceki dönem seçilerek o dönemin izin adedi ve uygulama öncesi kullanılan gün sayısı yazılabilir. Kullanılan izinler kalan izinden otomatik düşer. Sabahlama sonrası dinlenme günü yıllık izinden ve fazla mesaiden düşmez.

## Birden çok iş yeri

Uygulama tek bir firmaya bağlı değildir. Birden çok iş yeri eklenebilir. Her iş yerinin kayıtları, çalışma saatleri, yıllık izni ve fazla/eksik mesai toplamı ayrı tutulur.

## Mobil görünüm

Hafta tatili ayarında gün adı ve seçim işareti aynı kutu içinde, aynı satırda gösterilir. Form alanları, takvim özeti ve rapor tabloları dar telefon ekranlarında taşmayacak şekilde hizalanır. Gün kaydı ekranı sade tutulmuştur: Tarih, kayıt türü ve gün içindeki çalışma/izin aralıkları girilir; mola ile fazla/eksik süre otomatik hesaplanır. Hazır süre ekleme düğmeleri kullanılmaz; yalnızca **+ Çalışma Ekle** ve **+ Saatlik İzin Ekle** düğmeleri bulunur.

## Güvenlik ve Maaş

Alt menüdeki **Maaş** bölümü uygulama girişinden ayrı olarak yeniden kilitlenir. Uygulama ve Maaş için birbirinden farklı 4–6 haneli PIN’ler kullanılır; yedek PIN yoktur. İki PIN aynı olamaz ve yanlış deneme sayaçları da ayrı tutulur. Güvenlik bilgilerini belirlemek/değiştirmek, parmak izini kaydetmek/kaldırmak, iki aşamalı doğrulamayı değiştirmek veya kilidi kaldırmak için önce Uygulama PIN’i sorulur; Uygulama PIN’i henüz yoksa ilk kurulum doğrudan açılabilir. Üç yanlış denemede ilgili giriş önce 60 saniye kilitlenir ve ekranda geri sayım gösterilir; sonraki üç yanlış deneme gruplarında süre 120, 240 saniye şeklinde artar (en fazla 30 dakika). **Şifreyi Unuttum** bölümünde kurtarma şifresi doğrulanırsa ilgili Uygulama veya Maaş PIN’i yenilenebilir.

Parmak izi için güncel Chrome, HTTPS/PWA ve telefonda tanımlı ekran kilidi/parmak izi gerekir; indirilen HTML dosyasında çalışmayabilir. Ayarlar’daki **Parmak izi durumu** satırı kaydın durumunu gösterir. İki aşamalı doğrulama, parmak izi kaydı başarıyla tamamlanmadan açık görünmez. Kayıt tamamlandıktan sonra uygulama ve Maaş kilit ekranlarında **Parmak İziyle Aç** düğmesi görünür; iki aşamalı doğrulama açıksa önce ilgili PIN, sonra parmak izi istenir. Önceki sürümden yükseltmede kayıtlı ortak PIN, Uygulama PIN’i olarak korunur ve Maaş için ayrıca farklı bir PIN belirlenir. PIN tanımlı olmayan eksik güvenlik kayıtları uygulamayı kilitleyemez.

Maaş bölümünde yıl/ay bazında net maaş, brüt maaş, vergi iadesi, yan hak ve diğer ödemeler manuel eklenebilir. Ekranın altında toplam kazanç ve aylık ortalama gibi istatistikler gösterilir. Gelecek haklar bölümüne örneğin “0,5 Maaş İkramiyesi” yazıp tarihi eklenirse kalan gün sayısı gösterilir.

**Tazminat** bölümünde işe başlama tarihi ve son giydirilmiş brüt maaşa göre tahmini ihbar tazminatı, kıdem tazminatı ve kullanılmayan yıllık izin karşılığı hesaplanır. Kıdem tavanı elle yazılabilir veya internetten resmî ÇSGB e-bülteni kontrol edilerek güncellenebilir. Sonuç yalnızca tahmindir; kesin tutar ayrılma nedeni, bordro, vergi ve SGK durumuna göre değişir.

Maaş verileri yalnızca cihazda saklanır; GitHub eşitlemesine ve mesai yedeğine eklenmez. Kilit kayıtların görünmesini engeller ancak cihaz depolamasını teknik olarak şifrelemez.

## Rapor ve yedek

- Aylık, yıllık ve toplam fazla/eksik mesai istatistikleri
- Excel (CSV) raporu
- PDF / yazdırma
- Ayarlar → Veri Yönetimi bölümünde **Veri İndir**, **Yedek İndir** ve **Yedek Yükle**
- Verileri, fotoğraf ve belgeleri GitHub ile eşitleme

Fotoğraf ve belge dosyalarının kendisi JSON yedeğine eklenmez; GitHub eşitlemesiyle saklanabilir.

## Veri ve gizlilik

Kayıtlar telefonunuzda tutulur. GitHub eşitlemesinde yalnızca depo adı ve erişim anahtarı girilir; veriler kendi özel GitHub deponuza kaydedilir. GitHub erişim anahtarınız yalnızca cihazınızda saklanır; anahtarınızı kimseyle veya sohbetle paylaşmayın.

PIN/parmak izi kilidi, uygulamanın ve Maaş bölümünün başka kişiler tarafından açılmasını zorlaştırır ancak cihaz depolamasını şifrelemez. Kurtarma şifrenizi güvenli bir yerde saklayın.

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
