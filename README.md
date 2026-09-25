# Haven Connect

`connect.html` is the static browser page for local-only, same-Wi-Fi saves.

1. Open the page from a browser over HTTPS.
2. It creates a fresh `haven://connect` QR that is valid for thirty minutes.
3. In Haven Android, choose **Devices → Scan QR** and scan it.
4. The app advertises a short-lived `.local` address on the shared Wi-Fi and keeps the link endpoint on the phone.
5. The page connects directly to that local phone endpoint; pasted links are stored by Haven on the phone.
6. During that temporary session, a save sent from Haven to the connected browser appears as a small card under **Received from your phone**.

The page does not store or relay saves. It keeps a live local heartbeat so a closed browser tab is not presented as connected. It needs a current desktop browser that supports local-network access prompts (Chrome or Edge is the initial target). Both devices must use the same private Wi-Fi or phone hotspot, and Haven must remain open during the session.

`qrcode.js` is bundled from [qrcodejs](https://github.com/davidshimjs/qrcodejs) under the MIT license in `LICENSE-qrcodejs.txt`.
