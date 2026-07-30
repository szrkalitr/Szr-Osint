# Szr-Osint
🔍 SZR-OSINT



SZR-OSINT; kullanıcı adı, e-posta ve telefon numarası üzerinden açık kaynak istihbarat (OSINT) toplamak için yazılmış bir araçtır.

GitHub'dan tut Reddit'e, çeşitli platformlarda hedef hakkında veri toplar, eşleştirir ve tek raporda toplar.

---

⚡ Özellikler

- Kullanıcı adı tarama
- E-posta doğrulama
- Veri sızıntısı kontrolü
- Telefon numarası analizi
- Profil scraping
- Platform eşleştirme
- İlişkilendirme (Correlation)
- Hız limiti desteği
- Eşzamanlı tarama sistemi
- Konsol raporlama

---

📦 Kurulum

git clone https://github.com/szrkalitr/SZR-OSINT.git

cd SZR-OSINT

pip install -r requirements.txt

---

🚀 Kullanım

Sadece kullanıcı adı

python szr-osint.py -u hedefkullanici

Kullanıcı adı + e-posta

python szr-osint.py -u hedefkullanici -e hedef@mail.com

Kullanıcı adı + telefon

python szr-osint.py -u hedefkullanici -p +905551234567

Her şeyi tara

python szr-osint.py \
-u hedefkullanici \
-e hedef@mail.com \
-p +905551234567

---

⚙️ Parametreler

Parametre| Açıklama
"-u"| Hedef kullanıcı adı
"-e"| Hedef e-posta adresi
"-p"| Hedef telefon numarası
"--generate-emails"| Kullanıcı adından olası e-postalar üret
"--scan-services"| E-postanın kayıtlı olduğu servisleri tara
"--no-scraper"| Profil scraping sistemini kapat
"--concurrency"| Aynı anda gönderilecek istek sayısı
"--rate"| Saniye başına maksimum istek

---

🧪 Örnekler

Mail üret

python szr-osint.py -u semih --generate-emails

Servis taraması

python szr-osint.py -u semih -e semih@mail.com --scan-services

Scraper kapalı çalıştır

python szr-osint.py -u semih --no-scraper

Hızlı tarama

python szr-osint.py -u semih --concurrency 50 --rate 25

---

📂 Proje Yapısı

SZR-OSINT
│
├── config.py
├── szr-osint.py
├── correlation.py
├── report.py
├── net.py
│
├── core/
│   └── http_client.py
│
├── scanners/
│   ├── username.py
│   ├── email.py
│   └── phone.py
│
└── scrapers/

---

⚠️ Not

Bu araç büyü yapmak için değil.

Veri toplamak, hesap ilişkilendirmek ve OSINT araştırmalarını hızlandırmak için yazıldı.

Çıkan her sonuç doğru olacak diye bir şey yok, insan gibi kontrol etmeyi unutma.

---

Geliştirici

SZR Sec

GitHub: szrkalitr

"Tek sekmede bütün OSINT."
