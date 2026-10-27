# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.0.0

| Dosya / File | Boyut / Size | SHA-256 |
|---|---|---|
| [Ulak_1.0.0_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.0.0/Ulak_1.0.0_x64-setup.exe) | 3,65 MB | `a8539aeeeed4b7dacecb4ec0fa92e96fdf364e3aa170494f719664ed22ed2342` |

Windows 10 / 11, 64 bit. Microsoft Edge WebView2 gerekir (Windows 11'de hazır; yoksa kurulum
indirir). / Needs Microsoft Edge WebView2 (ready on Windows 11; otherwise the installer fetches it).

Kurulum dosyası imzalı değil; Windows SmartScreen uyarırsa "Ek bilgi" → "Yine de çalıştır".
The installer is not signed; if Windows SmartScreen warns, choose "More info" → "Run anyway".

Dosyayı doğrulamak için / To verify the file (PowerShell):

```powershell
Get-FileHash .\Ulak_1.0.0_x64-setup.exe -Algorithm SHA256
```

## Ulak 1.0.0 ile neler yapabilirsin / What Ulak 1.0.0 can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest ve OAuth 2.0 / Bearer, Basic, API key, Digest and OAuth 2.0
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
