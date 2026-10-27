# ⏱️ Mesai Takip — PWA (v3, genel kapsamlı / çok iş yerli)

Kişisel mesai takip uygulaması. Portföyüm uygulamasındaki gibi **telefona kurulabilen, internetsiz çalışabilen** modern bir PWA olarak hazırlandı. İlk aşama PWA'dır; istek üzerine sonraki aşamada APK'ya çevrilebilir.

## Çalışma düzeni (varsayılan)
- **Giriş:** 07:45 — **Çıkış:** 17:45 (Brüt 10 saat)
- **Molalar:** 10:00–10:10 çay (10 dk) • 12:15–12:55 yemek (40 dk) • 15:30–15:40 çay (10 dk) = **60 dk**
- **Günlük net hedef:** **9 saat**
- **Hafta sonu** (Cumartesi–Pazar) ve **resmi tatiller** hedefe dahil değil; o gün çalışılırsa tamamı fazla sayılır.
- Arife / 28 Ekim yarım gün hedefi (4,5 saat) hesaplanır. İşyeriniz tam tatil yapıyorsa o günü takvimden "Resmi Tatil" işaretleyin.
- Ücret hesabı **yoktur** — fazlalar **başa baş (1:1) saat bankasına** yazılır: 1 saat fazla = 1 saat kullanılabilir izin. Tamamı Ayarlar'dan değiştirilebilir.
- **Arife kuralı:** Arifeler/28 Ekim varsayılan yarım gün (4,5 saat) ama **arife günü uygulama açılışında sorar:** yarım gün / tam tatil / saat izniyle kapatma / yıllık izin / tam gün çalışma. Bir gün önceden ana sayfada "Yarın arife, yarın soracağım" uyarısı çıkar.

## v3 kapsamı
- **Çok iş yeri:** Üst çubukta iş yeri seçilir; her iş yerinin kayıtları, programı, yıllık izni ve saat bankası ayrıdır. Ayarlar > İş Yerlerim’den yeni iş yeri eklenir/arşivlenir. Bir kaydı düzenlerken başka iş yerine taşınabilir.
- **Geçmişe dönük giriş/düzeltme:** Takvim geçmiş ay/yıllara gider, “Geçmişe kayıt” butonu ve kayıt tarihi serbesttir. Eski kayda dokunup düzeltme/silme yapılabilir. Eldeki tablo **CSV aktar** ile toplu alınabilir (şablon indirilebilir); seçili aydaki boş iş günleri toplu normal mesai yapılabilir.
- **Kronometresiz akış:** Canlı başlat/bitir yoktur. “✓ Bugün normal çalışma yapıldı” normal günü yazar; “＋ Üstüne mesai ekle” ve editördeki +1/+2/+3/+4,5s kısayolları çıkışı uzatır. Çıkış saati zorunludur.
- **Tarihe duyarlı program:** Mola/çalışma/devir ayarları bir **yürürlük tarihiyle** program sürümü olarak kaydedilir. Her gün kendi tarihindeki programla hesaplanır; kaydedilen günün hedefi `targetSnapshot` ile dondurulur. Yeni ayar geçmişi geriye dönük değiştirmez (bilerek geçmiş yürürlük seçilirse kayıtsız günler etkilenebilir, uygulama uyarır).
- **Fotoğraf/belge ekleri:** Çalışma, şirket/zorunlu izin dahil her güne fotoğraf/PDF eklenir. Veriler IndexedDB’de saklanır; kayıt içinde yalnızca ek üst bilgisi durur. **Ekleri GitHub ile eşitle**, özel repoda `attachments/...` altına dosyaları gönderir/indirir. PDF için GitHub Contents API sınırı nedeniyle ~950 KB üstü yüklenmeyebilir; fotoğraflar otomatik sıkıştırılır. JSON yedeği ek dosyalarını içermez.
- **Rapor GitHub’a:** Rapor > “Raporu GitHub’a yükle”, `reports/<iş-yeri>/Mesai_Rapor_YYYY-MM.csv` ve `.md` özetini yükler. “Şimdi eşitle” daha yeni olan tarafı sorarak veri + ekleri eşitler.
- **İstatistik:** Aylık kartların yanında yıllık ve tüm zamanlar toplam fazla/eksik, net/hedef, tüm iş yerleri toplamı ve grafikler vardır.

## v2 kuralları
- **Akşam fazla mesaisi:** 17:45–18:15 akşam yemeği molasıdır. Çıkış 18:15 öncesi ise ekstra sayılmaz (gün 9s tamamlanmış olur); 18:15 sonrası süre bu 30 dk düşülerek ekstra yazılır.
- **Sabahlama:** İş geceye sarkarsa **02:00–02:40 gece molası** otomatik düşülür. Canlı kronometre gece yarısını geçse de ertesi sabah devam eder. Kaydı bitirince uygulama ertesi günü **maaş, yıllık izin ve saat bankasından kesinti olmadan** dinlenme yazmayı sorar (tip: *Sabahlama Ertesi Dinlenme*).
- **Saat bankası son kullanma:** Fazlalar **ay içinde** kullanılır. Ayın son **14 günü** kazanılanlar sonraki ayın **7. gününe** kadar devreder (Ayarlar > devir penceresi). Parti/parti takip edilir; süresi dolanlar raporda "⌛ Süresi doldu" ve ana sayfada uyarıyla görünür.
- **Notlar / iş günlüğü:** Her gün için büyük bir not alanı vardır. Çalışma gününde "Yapılan işler", izin gününde "Ne yaptım" olarak görünür; Kayıtlar'da notlardan arama yapılabilir, rapor/Excel çıktısında yer alır.
- **Yıllık izin:** Ayarlar'da yıla göre toplam hak + uygulamadan önce kullanılan yazılır. Yıllık izin günleri otomatik düşer (hafta içi 1, arife 0,5, tatil/hafta sonu 0; kayıt içinde değiştirilebilir). Kalan ana sayfada ve istatistikte izlenir.
- **İstatistik:** Rapor'da yıllık aylara göre grafik ve tüm zamanlar toplamları, sabahlama sayısı, en yoğun ay, ortalama/en uzun gün vb.
- **GitHub / URL senkronu:** Ayarlar'daki alana özel bir GitHub repo, dal, dosya yolu ve sadece o repoya **Contents Read/Write** yetkili fine-grained token yazılır. Oradan veri çekilir ve GitHub'a kaydedilir; isterseniz sadece **raw URL'den çekme** de yapılabilir. Token yalnızca cihazda saklanır, senkron dosyasına yazılmaz. Tokenları asla sohbete göndermeyin.
- **Şifre kilidi:** İlk açılışta kurulum sorulur. Şifre cihazda özet (hash) olarak saklanır; uygulama girerken ve 2 dakikadan uzun arka planda kalınca kilitlenir. Kilit gizlilik amaçlıdır, veriyi şifrelemez. Koyu/açık tema mevcuttur.

## Özellikler
- ▶️ **Canlı kronometre:** tek tuşla başlat/bitir, molalar net süreden otomatik düşülür, hedefe kalan / fazla süre canlı görünür
- 📅 **Takvim:** renkli gün durumları, resmi tatil/hafta sonu otomatik, dokununca kayıt düzenleme
- 📋 **Kayıtlar:** manuel giriş-çıkış, izin/rapor/tatil işaretleme, kayıtsız günleri toplu "normal mesai" ile doldurma
- ⏳ **Saat Bankası (1:1):** fazla çalışmalar bankaya "+"; tam gün/yarım gün/saatlik **Saat İzni** veya erken çıkışta "eksik kısmı bankadan karşıla" bankadan "−" düşer. Toplam bakiye ay sonunda sıfırlanmaz, devreden başlangıç bakiyesi Ayarlar'dan girilebilir. "50 saat ≈ 5 tam gün + 5 saat" gibi gün karşılığı da gösterilir.
- 📊 **Rapor:** aylık çalışma/hedef/bakiye/fazla/eksik, saat bankası hareket dökümü, günlük grafik, **Excel (CSV)** indirme, **PDF/yazdırma**
- 💾 **Yedek:** JSON yedek indir / geri yükle (telefon değişiminde kullanın)
- 🌙 Koyu/açık tema, telefona uygun alt menü, veriler cihazda saklanır (sunucu yok)

## Dosyalar
| Dosya | Açıklama |
|---|---|
| `index.html` | Uygulamanın tamamı (tek dosya çalışır) |
| `manifest.webmanifest` | Telefon kurulum bilgisi |
| `sw.js` | Çevrimdışı çalışma (service worker) |
| `icon-192.png`, `icon-512.png` | Uygulama simgeleri |

> **Not:** `index.html`'i tek başına açsanız bile uygulama çalışır. Ancak telefona "kurulum" ve çevrimdışı için 4 dosyanın birlikte **HTTPS** bir adreste olması gerekir (aşağıda).

## Kalıcı olarak telefona kurmak için yayınlama (5 dk, ücretsiz)
Canlı önizleme bağlantısı geçicidir. Kalıcı kullanım için klasörü ücretsiz bir yere yükleyin:

### Seçenek A — Netlify Drop (en kolay)
1. Bilgisayarda https://app.netlify.com/drop adresini açın (ücretsiz hesap açılır)
2. `mesai-takip` klasörünün **içindeki dosyaları** (veya klasörü) sayfaya sürükleyip bırakın
3. Size `https://....netlify.app` adresi verilir → telefonda açın → **Kur / Ana Ekrana Ekle**

### Seçenek B — GitHub Pages
1. GitHub'da yeni repo açın, dosyaları yükleyin
2. Settings → Pages → Branch: `main` → Save
3. Verilen adresi telefonda açıp kurun

### Kurulum
- **Android (Chrome):** ⋮ menü → **Uygulamayı yükle / Ana ekrana ekle**
- **iPhone (Safari):** Paylaş ⬆️ → **Ana Ekrana Ekle**

## Veri güvenliği
Veriler yalnızca telefon tarayıcısında (`localStorage`) saklanır, hiçbir sunucuya gitmez.
Tarayıcı verilerini silmek / telefon değiştirmek veriyi silebilir: ayda bir **Rapor → Yedek indir (JSON)** yapıp dosyayı saklayın.

## Resmi tatiller
Ulusal bayramlar her yıl otomatik eklenir. Dini bayramlar 2025–2026 için tanımlıdır (2026: Ramazan 19–22 Mart, Kurban 26–30 Mayıs).
Farklı yıllar/günler için takvimden o günü **Resmi Tatil** olarak işaretlemek yeterlidir.
