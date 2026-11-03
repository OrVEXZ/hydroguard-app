HYDROGUARD PWA — SETUP

Files:
- index.html: responsive dashboard
- manifest.webmanifest: installable app metadata
- service-worker.js: caches the app shell
- icon-192.png and icon-512.png: temporary install icons

API:
https://hydroguard-live-api.anamikasathish09.workers.dev/readings

The app polls GET /readings every 5 seconds. It expects numeric fields:
upstream, downstream, rain, wallHealth.

PUBLISH AND INSTALL:
1. Extract this ZIP.
2. Upload all three app files to a GitHub repository, keeping index.html at the repository root.
3. Enable GitHub Pages for that repository.
4. Open the HTTPS Pages address on your Android phone.
5. In Chrome, open the menu and choose "Install app" or "Add to Home screen".

IMPORTANT:
- This build displays live readings and alert conditions. Pump buttons are intentionally disabled because the current Worker has no secure pump-command endpoint and relay operation has not yet been verified.
- The original HydroGuard logo was not attached to this work session. A temporary H mark is used; replace it with the exact logo when supplied.
- The app shell can be cached, but live readings require internet.
- Water status mapping assumes the firmware maps 0–2.20 cm to 0–100%.
- The wallHealth field is treated as the wall-moisture percentage for the seepage condition (>60%).
