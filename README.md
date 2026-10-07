# Crew List Scanner

**Use it on a phone:** open https://johann-kruger.github.io/crew-list-scanner/ in Safari (iPhone) or Chrome (Android), then Share → Add to Home Screen. After the first open it works with no signal.

Skippers photograph each crew member's passport or SA ID; the app reads the
name, nationality and document number on the phone (no internet needed) and
builds a crew list that can be copied or shared as a CSV.

- `www/index.html` — the app itself
- `www/ocr/`, `www/vendor/` — bundled reader (Tesseract OCR, ZXing barcodes)
- `ios/` — Xcode project (see BUILD_IOS.md)
- `android/` — Android Studio project

## Updating the web version

Edit `www/`, bump `VERSION` in `www/sw.js`, push to `main`. GitHub publishes it automatically; phones pick it up next time they open the app with signal.
