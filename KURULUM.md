# Zikirmatik – APK'yı oluşturma ve telefona kurma

Bu klasör, Zikirmatik v3'ü Android uygulamasına çeviren hazır bir projedir.
APK'yı GitHub ücretsiz olarak derler. Bilgisayara Android Studio kurmanız gerekmez.

## 1. GitHub'a yükleme (bir kez)
1. https://github.com adresinde ücretsiz bir hesapla giriş yapın.
2. Sağ üstte **+ → New repository** deyin, adı `zikirmatik` olsun, **Create repository**'ye basın.
3. Açılan sayfada **uploading an existing file** bağlantısına tıklayın.
4. Bu klasörün **içindekileri** (app, .github, build.gradle, settings.gradle, gradle.properties...) sürükleyip bırakın, **Commit changes** deyin.
   - `.github` klasörü gizli olduğu için bazı bilgisayarlarda sürüklenmeyebilir. Yüklemeden sonra depoda `.github/workflows/build-apk.yml` dosyasını göremiyorsanız:
     **Add file → Create new file** deyin, dosya adı kutusuna `.github/workflows/build-apk.yml` yazın (eğik çizgiler klasör açar) ve bu klasördeki `build-apk.yml` dosyasının içeriğini yapıştırıp Commit edin.

Git kullanıyorsanız: `git init`, `git add .`, `git commit -m ilk`, `git branch -M main`, `git remote add origin <depo-adresi>`, `git push -u origin main`.

## 2. APK'yı indirme
1. Depoda **Actions** sekmesine girin. "APK derle" çalışmaya başlar (yaklaşık 3-5 dakika).
2. Yeşil tik çıkınca o çalışmaya tıklayın, en altta **Zikirmatik-APK** dosyasını indirin (zip içinde `app-debug.apk`).
3. Çalışmıyorsa **Actions → APK derle → Run workflow** ile elle başlatabilirsiniz.

## 3. Telefona kurma
1. `app-debug.apk` dosyasını telefona gönderin (WhatsApp, Drive, kablo).
2. Dosyaya dokunun. Telefon "bilinmeyen kaynaklardan yükleme" izni isterse bu uygulama için izin verin.
3. Yüklenince ana menüde **Zikirmatik** simgesi çıkar.

Gereken: Android 8.0 veya üstü.

## Notlar
- Sayaç, ayarlar ve geçmiş uygulamanın içinde saklanır. Uygulamayı silerseniz bunlar da silinir.
- Titreşim ve "ekran açık kalsın" doğrudan telefonun kendi özellikleriyle çalışır.
- Zikir ekranını değiştirmek için `app/src/main/assets/index.html` dosyası değiştirilir, depoya yüklenince yeni APK otomatik derlenir.
