# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.3.0

| Dosya / File | Platform | Boyut / Size | SHA-256 |
|---|---|---|---|
| [Ulak_1.3.0_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.3.0/Ulak_1.3.0_x64-setup.exe) | Windows 10 / 11, 64 bit | 4,43 MB | `2977727a8f303c0c14b118afe7be535f6b9f9fba52588c2447b4fc5ee4e95e30` |
| [Ulak_1.3.0_universal.dmg](https://github.com/mozkurt27/ulak-releases/releases/download/v1.3.0/Ulak_1.3.0_universal.dmg) | macOS 10.15+, Apple Silicon + Intel | 12,01 MB | `2d7cb08d08af382df54ec98a068137ca6db6290ab69e9b5bd1b8ce7ca0a65ca1` |

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
Get-FileHash .\Ulak_1.3.0_x64-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 Ulak_1.3.0_universal.dmg
```

## Ulak 1.3.0'da neler değişti / What changed in 1.3.0

- Collection Runner: koleksiyon ya da klasörü sırayla çalıştır; tekrar, bekleme, CSV/JSON veri dosyası, setNextRequest; sonuçları JSON olarak dışa aktar / Collection Runner: run a collection or folder in order; iterations, delay, CSV/JSON data file, setNextRequest; export the results as JSON
- Script'lerde pm.sendRequest (callback ve await) / pm.sendRequest in scripts (callback and await)
- Kod olarak al: cURL, JavaScript, Node.js, Python, C#, Go, Java, PHP, HTTPie / Get as code: cURL, JavaScript, Node.js, Python, C#, Go, Java, PHP, HTTPie
- Proxy (sistem ya da elle) ve istemci sertifikası (mTLS) ayarları / Proxy (system or manual) and client certificate (mTLS) settings
- Cookie yöneticisi; cookie'ler uygulama kapanınca silinmiyor / Cookie manager; cookies stay when the app closes
- AWS Signature auth / AWS Signature auth
- Uygulama içi güncelleme: yeni sürüm çıkınca sorar, onaylarsan kurar; 1.2.0'dan 1.3.0'a bir kez elle geçilir / In-app updates: asks when a new version is out and installs it if you agree; moving from 1.2.0 to 1.3.0 is manual once
- Yedeğe globals ve ayarlar da giriyor; proxy ve sertifikalar bilgisayarda kalıyor / Backups now include globals and settings; proxy and certificates stay on the computer

## Ulak ile neler yapabilirsin / What Ulak can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest, OAuth 2.0 ve AWS Signature / Bearer, Basic, API key, Digest, OAuth 2.0 and AWS Signature
- Collection Runner ve kod üretme / Collection Runner and code snippets
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
