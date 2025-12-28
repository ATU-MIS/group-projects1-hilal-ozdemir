[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/7jTrgXmk)
1. Kullanıcı Uçuş Rezervasyon Akışı
Bu diyagram, bir kullanıcının giriş yapmasından biletini alıp uçuş sonrası hizmetlere erişmesine kadar olan ana yolu temsil eder.

Akış Adımları:
Giriş: Kullanıcı e-posta/şifre gönderir -> Sistem DB'den doğrular -> Ana Panel açılır.

Arama: Kullanıcı (Kalkış, Varış, Tarih, Yolcu, Sınıf) kriterlerini girer -> Sistem uygun uçuşları listeler.

Seçim: Kullanıcı uçuşu ve ardından koltuğu seçer.

Ödeme & Onay: Kullanıcı ödeme bilgilerini iletir -> Sistem ödemeyi onaylar -> Bilet bilgisi bildirimi gönderilir ve Seyahat Rehberi sunulur.

2)Uçuş Sonrası: Kullanıcı sistem üzerinden uçuş sonrası hizmetlere erişir.
Admin kullanıcısı, sistemin arka planındaki verileri yönetmek için sisteme dahil olur.
Aktör , İşlem,    Hedef Veri
Admin,  Giriş Yap,  Admin Paneli
Admin,  CRUD (Ekle/Sil/Güncelle),  Uçuşlar & Rezervasyonlar
Admin,  Paket Tanımlama,     Sigorta Paketleri
Admin,  Yetkilendirme,      Kullanıcı Yönetimi

3. Alternatif Senaryolar (Hata ve Bildirimler)
Sistemde her zaman işler yolunda gitmeyebilir. Bu durumlar için Alt (Alternative) akışlar devreye girer.

Ödeme Başarısız: Ödeme ağ geçidinden "Red" yanıtı gelirse, sistem kullanıcıya "Ödeme Başarısız" hatası döner ve tekrar ödeme adımına yönlendirir.

Uçuş Rötarı: Admin veya Otomasyon Sistemi uçuş saatini güncellediğinde, sistem otomatik olarak tetiklenir ve kullanıcıya SMS/Sistem Bildirimi gönderir.
