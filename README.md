# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.1.0

| Dosya / File | Platform | Boyut / Size | SHA-256 |
|---|---|---|---|
| [Ulak_1.1.0_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.1.0/Ulak_1.1.0_x64-setup.exe) | Windows 10 / 11, 64 bit | 3,73 MB | `3ed143b6e793660ed05c2e4f2152a4be7dd050b7710bd31cdabda812f3d1a842` |
| [Ulak_1.1.0_universal.dmg](https://github.com/mozkurt27/ulak-releases/releases/download/v1.1.0/Ulak_1.1.0_universal.dmg) | macOS 10.15+, Apple Silicon + Intel | 10,22 MB | `a1820748211c60472203f40dd1f19e0749797fb9724d6f0ab1fdc1fd4fff3210` |

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
Get-FileHash .\Ulak_1.1.0_x64-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 Ulak_1.1.0_universal.dmg
```

## Ulak 1.1.0'da neler değişti / What changed in 1.1.0

- İsteğe bağlı hesap: uygulamadan kayıt, mail koduyla doğrulama, şifremi unuttum; giriş yapanın adı sağ üstte / Optional account: sign up in the app, verify with an e-mailed code, reset a forgotten password; your name shows at the top right
- Collection ve environment sync'i: Ulak sunucusuna ya da seçtiğin bir klasöre, hesabının anahtarıyla şifreli / Collection and environment sync: to the Ulak server or a folder you pick, encrypted with your account's key
- Açılışta ve saatte bir otomatik sync; çakışmada son değişiklik kazanır, diğer hali çöp kutusunda kalır / Automatic sync at start and every hour; the latest change wins, the other version stays in the trash
- Sync geçmişi / Sync history

## Ulak ile neler yapabilirsin / What Ulak can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest ve OAuth 2.0 / Bearer, Basic, API key, Digest and OAuth 2.0
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
