# Haven Connect

`index.html` is the static browser page for local-only, same-Wi-Fi saves.

This repository is deliberately safe to make public for GitHub Pages. It contains
only the static QR page and its QR-code library; it contains no Haven Android
source, APK, saved links, account details, session data, or server.

1. Open the page from a browser over HTTPS.
2. It creates a fresh `haven://connect` QR that is valid for ten minutes.
3. In Haven Android, choose **Devices → Scan QR** and scan it.
4. The app advertises a short-lived `.local` address on the shared Wi-Fi and keeps the link endpoint on the phone.
5. The page connects directly to that local phone endpoint; pasted links are stored by Haven on the phone.

The page does not store or relay saves. It needs a current desktop browser that supports local-network access prompts (Chrome or Edge is the initial target). Both devices must use the same private Wi-Fi or phone hotspot, and Haven must remain open during the session.

`qrcode.js` is bundled from [qrcodejs](https://github.com/davidshimjs/qrcodejs) under the MIT license in `LICENSE-qrcodejs.txt`.
