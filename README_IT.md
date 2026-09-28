# TOGG Deneyim Merkezi Çorlu – Servis Takip ve Yönetim Sistemi
## IT Teslim Paketi – 2026

### Amaç
Servis operasyonlarının tek web uygulamasında takip edilmesi; inceleme, atölye, parça bekleme, teslimat, ikame, randevu, çekici, sıfır araç teslimatı, stok ve işlem geçmişinin yönetilmesi.

### Mevcut durum
Paket, mevcut uygulama çalışmasını, örnek Excel veri kaynağını ve IT incelemesi için teknik dokümantasyonu içerir. Kurumsal canlı entegrasyon henüz yapılmamıştır.

### Hedef mimari
Kurumsal veri kaynağı / onaylı API → uygulama backend'i → uygulama veritabanı → web arayüzü.

Doğrudan kurumsal veritabanı erişimi yerine IT tarafından onaylanan API, web servis, read-only erişim veya kurumun uygun gördüğü başka bir entegrasyon yöntemi tercih edilmelidir.

### Ana modüller
Yönetim Paneli; İnceleme Süreci; Atölye İşlemde; Parça Bekliyor; Teslim Edilecek; İkame; Yedek Parça; Randevular; Sıfır Araç Teslimat; Çekici ile Gelenler; Bildirimler; İşlem Geçmişi; Kullanıcı/Yetkilendirme Yönetimi.

### Temel iş akışı
İnceleme → Atölye → Parça Bekliyor (gerekiyorsa) → Teslim Edilecek → Tamamlandı.

### Veri modeli
Akıllı cihaz kaydında temel olarak plaka, VIN/şasi, model (T10X/T10F), batarya tipi, kullanıcı bilgileri, geliş şekli, süreç, işlem detayları ve geçmiş bilgileri tutulması planlanmaktadır.

### Yetkilendirme
Tüm kullanıcılar ekranları görüntüleyebilir; düzenleme yetkisi modül bazında sınırlandırılır. Yetkisiz düzenleme mesajı: “Bu bölüm için düzenleme yetkiniz bulunmuyor.” Kullanıcı ve yetki yönetimi yalnızca yetkili yönetici tarafından yapılmalıdır. Yetki değişiklikleri audit log'a yazılmalıdır.

### Güvenlik / IT beklentisi
- Kurumsal kimlik doğrulama yöntemi IT tarafından belirlenmeli.
- Parolalar ve secret'lar kaynak koda/açık veri dosyalarına konulmamalı.
- Üretimde HTTPS kullanılmalı.
- Kurumsal veriye en az yetki prensibiyle erişilmeli.
- Mümkünse test/sandbox ortamı kullanılmalı.
- Kullanıcı, zaman, işlem ve değişiklik bilgilerini içeren audit log tutulmalı.

### IT'den talep edilen
1. Kullanılabilir API/web servis var mı?
2. Hangi alanların paylaşılmasına izin veriliyor?
3. Test ortamı var mı?
4. Kimlik doğrulama yöntemi nedir?
5. Uygulama şirket ağı/VPN içinde mi çalışmalı?
6. Kurumun onayladığı hosting yöntemi nedir?
7. Veri saklama ve loglama gereksinimleri nelerdir?
8. Güvenlik/pentest veya kod inceleme süreci gerekiyor mu?

### Paket içeriği
- `Uygulama/` : mevcut web uygulaması kaynakları
- `Veri_Ornegi/TOGG_DENEYIM_MERKEZI_CORLU_OTOMATIK_TAKIP_V2.xlsx` : mevcut Excel tabanlı örnek veri/workflow
- Bu README: IT inceleme ve entegrasyon notları

### Önemli not
Bu paket kurumsal sistemlere erişim bilgisi içermez. Canlı şirket verisi entegrasyonu yalnızca şirket IT/güvenlik onayı ve kurumun belirlediği erişim yöntemi üzerinden yapılmalıdır.

Geliştiren: Aleyna Uzun
TOGG Deneyim Merkezi Çorlu
2026
