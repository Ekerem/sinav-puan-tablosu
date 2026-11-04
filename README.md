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

## Güncelleme
- **Web:** "🔄 Güncelle" sayfayı en yeni sürümle yeniden yükler.
- **APK (canlı güncelleme):** Uygulama açılışta GitHub Pages'teki `version.json`'a bakar, yeni sürümün `index.html`'ini indirip
  telefonda saklar ve bir sonraki açılışta (ya da "Şimdi geç" / "Güncelle" ile hemen) APK yeniden kurulmadan ona geçer.
  Kayıtlar aynı yerde kalır. Açılamayan bir kopya bir sonraki açılışta atılır, APK'nın içindeki sürüm açılır.
- Yeni APK yalnızca `version.json` içindeki `apkMin` artırıldığında istenir. Bunu yalnız yeni bir Android eklentisi
  ya da `index.html` dışında yeni bir dosya eklendiğinde yap.

## Yeni sürüm çıkarmak
`web/index.html` içindeki `APP_VERSION` ve `web/version.json` içindeki `version` aynı anda artırılır ve `main`'e gönderilir.
Pages iş akışı yayınlar; APK iş akışı yeni kurulumlar için `v1.x.y` Release'ini de oluşturur.

Made by Us
