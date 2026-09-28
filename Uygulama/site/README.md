# TOGG Deneyim Merkezi Çorlu — Servis Takip ve Yönetim Sistemi

Bu sürüm, konuşulan modüllerin web uygulaması çekirdeğini içerir: güvenli oturum, rol/yetki, 98 cihaz seed verisi, süreç otomasyonu, randevu, ikame, çekici, sıfır araç teslimat, yedek parça, bildirim ve audit log.

## Render + PostgreSQL
1. GitHub'a bu klasördeki tüm dosyaları yükleyin.
2. Render'da PostgreSQL oluşturun.
3. Web Service oluşturup GitHub reposunu bağlayın.
4. Build command: `npm install`
5. Start command: `npm start`
6. Environment variables:
   - `DATABASE_URL` = Render PostgreSQL internal connection string
   - `JWT_SECRET` = uzun, rastgele gizli değer
7. Deploy edin.

İlk açılışta seed kullanıcılar ve Excel'den aktarılmış 98 cihaz kaydı oluşturulur. Production'da ilk giriş şifreleri hemen değiştirilmelidir.
