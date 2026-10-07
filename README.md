# Crew List Scanner

Skippers photograph each crew member's passport or SA ID; the app reads the
name, nationality and document number on the phone (no internet needed) and
builds a crew list that can be copied or shared as a CSV.

- `www/index.html` — the app itself
- `www/ocr/`, `www/vendor/` — bundled reader (Tesseract OCR, ZXing barcodes)
- `ios/` — Xcode project (see BUILD_IOS.md)
- `android/` — Android Studio project
