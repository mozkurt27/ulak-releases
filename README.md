# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.0.2

| Dosya / File | Platform | Boyut / Size | SHA-256 |
|---|---|---|---|
| [Ulak_1.0.2_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.0.2/Ulak_1.0.2_x64-setup.exe) | Windows 10 / 11, 64 bit | 3,66 MB | `b9819a1b169afc64e6bdbb9e501178b9f512230790537565a4bd4729eb72edb5` |
| [Ulak_1.0.2_universal.dmg](https://github.com/mozkurt27/ulak-releases/releases/download/v1.0.2/Ulak_1.0.2_universal.dmg) | macOS 10.15+, Apple Silicon + Intel | 10,04 MB | `7705b3664e522a486c25ab99adfb130d3473862f94083c057da678ce0e555a93` |

**Windows:** Microsoft Edge WebView2 gerekir (Windows 11'de hazır; yoksa kurulum indirir).
Kurulum dosyası imzalı değil; SmartScreen uyarırsa "Ek bilgi" → "Yine de çalıştır".
Needs Microsoft Edge WebView2 (ready on Windows 11; otherwise the installer fetches it). The
installer is not signed; if SmartScreen warns, choose "More info" → "Run anyway".

**macOS:** Ulak'ı Applications klasörüne sürükle. Uygulama ücretli bir Apple geliştirici
hesabıyla imzalanmadı; ilk açılışta macOS uyarırsa Sistem Ayarları → Gizlilik ve Güvenlik →
"Yine de Aç". Drag Ulak to Applications. The app is not signed with a paid Apple developer
account; if macOS warns on the first start, open System Settings → Privacy & Security →
"Open Anyway".

Dosyayı doğrulamak için / To verify a file:

```powershell
Get-FileHash .\Ulak_1.0.2_x64-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 Ulak_1.0.2_universal.dmg
```

## Ulak 1.0.2'de neler değişti / What changed in 1.0.2

- Görsel dönen cevaplar (PNG, JPEG, GIF, WebP …) Body'de görsel olarak gösteriliyor / Image responses (PNG, JPEG, GIF, WebP …) are shown as a picture in Body
- Dosyaya kaydet görseli kendi uzantısıyla kaydediyor / Save to file keeps the image's own extension

## Ulak ile neler yapabilirsin / What Ulak can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest ve OAuth 2.0 / Bearer, Basic, API key, Digest and OAuth 2.0
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
