# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.4.0

| Dosya / File | Platform | Boyut / Size | SHA-256 |
|---|---|---|---|
| [Ulak_1.4.0_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.4.0/Ulak_1.4.0_x64-setup.exe) | Windows 10 / 11, 64 bit | 4,44 MB | `c5ef2d463c280e0c7e894756f9d5c836b90e487e19223642223ea835c83a5e87` |
| [Ulak_1.4.0_universal.dmg](https://github.com/mozkurt27/ulak-releases/releases/download/v1.4.0/Ulak_1.4.0_universal.dmg) | macOS 10.15+, Apple Silicon + Intel | 12,03 MB | `78df85d4574825075bcac08bf5367530e19cadc30cdc04085c862401ae94f4fd` |

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
Get-FileHash .\Ulak_1.4.0_x64-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 Ulak_1.4.0_universal.dmg
```

## Ulak 1.4.0'da neler değişti / What changed in 1.4.0

- Yedekler önce sıkıştırılıp sonra şifreleniyor; yaklaşık 10 kat az yer / Backups are compressed, then encrypted; about 10 times smaller
- Son 7 günün yedeği tutuluyor / The last 7 days of backups are kept
- Ulak sunucusunda hesap başına 5 MB; sığmazsa yedekleri Local'e al / 5 MB per account on the Ulak server; if it does not fit, keep backups in a folder (Local)
- 30 gün yedek gelmeyen hesabın sunucu yedekleri siliniyor; klasördekiler silinmiyor / An account with no backup for 30 days loses its server backups; folder backups are never removed
- 1.3.0 kuruluysa Ulak bu güncellemeyi kendisi önerir / With 1.3.0 installed, Ulak offers this update itself

## Ulak ile neler yapabilirsin / What Ulak can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest, OAuth 2.0 ve AWS Signature / Bearer, Basic, API key, Digest, OAuth 2.0 and AWS Signature
- Collection Runner ve kod üretme / Collection Runner and code snippets
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
