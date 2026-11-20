# Ulak - indirmeler / downloads

Ulak, bilgisayarında çalışan bir API istemcisi. Bu depo yalnızca kurulum dosyalarını tutar.
Ulak is an API client that runs on your computer. This repository only holds the installers.

Site: https://ulak-client.duckdns.org

Tüm sürümler / All releases: https://github.com/mozkurt27/ulak-releases/releases

## Son sürüm / Latest: 1.2.0

| Dosya / File | Platform | Boyut / Size | SHA-256 |
|---|---|---|---|
| [Ulak_1.2.0_x64-setup.exe](https://github.com/mozkurt27/ulak-releases/releases/download/v1.2.0/Ulak_1.2.0_x64-setup.exe) | Windows 10 / 11, 64 bit | 3,78 MB | `471d874872077c2f586690a58eb2e9cc931c39765082a725482b03efc3f1388f` |
| [Ulak_1.2.0_universal.dmg](https://github.com/mozkurt27/ulak-releases/releases/download/v1.2.0/Ulak_1.2.0_universal.dmg) | macOS 10.15+, Apple Silicon + Intel | 10,32 MB | `f9ed0332ec54bcfdf97e06c6951399cab11f27e7b40911e1d482c6b01369f2bc` |

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
Get-FileHash .\Ulak_1.2.0_x64-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 Ulak_1.2.0_universal.dmg
```

## Ulak 1.2.0'da neler değişti / What changed in 1.2.0

- Hesap kodları artık gerçekten maile gidiyor / Account codes now really go out by e-mail
- Sync yerine günlük yedek: açılışta ve saatte bir yalnız değişenler, son 30 gün; Ulak sunucusunda hesap başına 256 MB, klasörde sınır yok / Daily backups instead of sync: at start and every hour, only what changed, the last 30 days; 256 MB per account on the Ulak server, no limit in a folder
- Yedekten yükle: kaynağı ve günü seç, collection ve environment'ları listeden işaretle; Ulak'ta olanın üzerine yazmadan önce sorar, eski hali çöp kutusuna kopyalar / Restore from backup: pick the source and the day, tick items from the list; asks before replacing and copies the old version to the trash
- Yedek yerini değiştirince günler yeni yere taşınır; sunucudan klasöre geçince sunucudaki yedek silinir / Changing where backups go moves the days there; moving from the server to a folder deletes the server's copy
- 1.1.0'ın sync'i yeni sunucuyla çalışmaz; 1.2.0'a güncelle / 1.1.0's sync does not work with the new server; update to 1.2.0

## Ulak ile neler yapabilirsin / What Ulak can do

- Postman koleksiyon ve environment dosyalarını kayıpsız içe ve dışa aktarma / Import and export Postman collections and environments without loss
- Swagger/OpenAPI belgesinden ve cURL komutundan istek oluşturma / Create requests from a Swagger/OpenAPI document or a cURL command
- Environment, koleksiyon ve global değişkenler / Environment, collection and global variables
- Bearer, Basic, API key, Digest ve OAuth 2.0 / Bearer, Basic, API key, Digest and OAuth 2.0
- pm.* pre-request ve test script'leri / pm.* pre-request and test scripts
- Server-Sent Events, NDJSON akışları ve WebSocket / Server-Sent Events, NDJSON streams and WebSocket
- Gönderim geçmişi, komut paleti, dört tema, Türkçe ve İngilizce arayüz / Send history, command palette, four themes, Turkish and English interface
