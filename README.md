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

## 1.0.0 ile gelenler / New in 1.0.0

- cURL komutundan içe aktarma / Import from a cURL command
- Digest ve OAuth 2.0 (client credentials, password, authorization code + PKCE)
- Server-Sent Events ve NDJSON akışları / streams, event by event
- WebSocket istekleri ve kayıtlı mesajlar / WebSocket requests and saved messages
- Türkçe ve İngilizce arayüz / Turkish and English interface
