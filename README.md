# Sınav Puan Tablosu

Öğretmenin sınav puanlarını soru soru girdiği, toplamı ve sınıf ortalamasını otomatik hesaplayan tablo.
Puanlar klavyeyle ya da **sesle** girilebilir.

- Soru sayısı ve her sorunun puanı ayarlanır (toplam 100 değilse uyarır).
- Öğrenci listesi e-Okul / Excel'den yapıştırılabilir.
- Her soru için ortalama ve başarı yüzdesi, her öğrenci için toplam.
- Birden çok sınav kaydedilir; yeni sınav aynı öğrenci listesiyle açılır.
- "Excel'e kopyala" ile tablo Excel'e / e-Okul'a yapıştırılır, web sürümünde CSV indirilebilir.

## Sesle giriş
Mikrofona bas, seçili hücreden itibaren puanları söyle: `15`, `sekiz buçuk`, `tam`, `geç`, `geri`, `sil`, `dur`.
Öğrenci adı söylenince ona atlar (`Ayşe 10 8 15`), `3. soru 12` o soruya atlayıp yazar.
Sorunun puanından büyük sayı yazılmaz. Web'de Chrome'un ses tanıması, APK'da Android'in ses tanıması
(`@capacitor-community/speech-recognition`) kullanılır.

## Bağlantılar
- Uygulama (GitHub Pages): https://ekerem.github.io/sinav-puan-tablosu/
- APK indir: https://github.com/Ekerem/sinav-puan-tablosu/releases/latest/download/sinav-puan-tablosu.apk

## Yeni sürüm
`web/index.html` içindeki `APP_VERSION` ve `web/version.json` aynı anda artırılır ve `main` dalına gönderilir.
APK iş akışı sürümü `version.json`'dan okuyup `v1.0.1` gibi bir Release oluşturur.

Made by Us
