# Yapay zekâ orkestrası

- Şef modeli: `gpt-6.1-sol`, akıl yürütme düzeyi `medium`. Proje ayarı `.codex/config.toml` içindedir.
- İşi büyüklüğüne göre böl. Bağımsız alt görevler için uygun özel ajanı açıkça çağır; kısa veya birbirine bağımlı adımları şef tamamlayabilir.
- Ajan brifinde GÖREV, SENİN DOSYALARIN, DOKUNMA, ÖNCE OKU, BİTTİ TANIMI ve RAPOR başlıklarını kullan.
- Mekanik iş: `yukleyici` (`gpt-6-luna`, low). Araştırma ve tarif edilmiş kod: `arastirmaci` veya `gelistirici` (`gpt-6-luna`, medium). Tasarım ve video: `tasarimci` veya `video-ureticisi` (`gpt-6.1-sol`, medium).
- Orta ve büyük değişiklikte işi yapan ajandan ayrı `denetci` (`gpt-6-luna`, high) kullan. Güvenlik, ödeme, mahremiyet veya veri kaybı riski varsa `denetci-riskli` (`gpt-6.1-sol`, medium) seç. Küçük değişiklikte diff'i şef inceleyebilir.
- Aynı dosyaya eşzamanlı yazan ajan başlatma. Paralel yazma gerekiyorsa ayrı çalışma kopyaları ve dallar kullan; sonuçları birleştirmeden önce diff'i ve testleri kontrol et.
- DÜZELT kararında engelleri giderip yeniden denetlet; üç tur sonunda sürüyorsa kullanıcıya somut engeli bildir.
- Kaynak, tarih, sayı ve test sonucu uydurma. Son raporda yapılan işi, doğrulama sonucunu ve açık riskleri belirt.
- Kullanıcı açıkça istemedikçe ek bir workflow veya çok ajanlı denetim zinciri başlatma.
