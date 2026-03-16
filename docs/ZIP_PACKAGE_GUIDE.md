# ZIP Package Guide — Aesthetic Clinic Website System

How to create the final sellable ZIP file for Gumroad, Lemon Squeezy, or direct sale.

---

## Files to INCLUDE in the ZIP

### HTML Pages (16 files)
```
the-ultimate-beauty-homepage.html
kezelesek.html
konzultacio.html
protocol.html
the-ultimate-beauty-protocol.html
protocol-treatments.html
protocol-hialuronsav-szinergia.html
clinical-program.html
technologia.html
technologia-hub-new.html
technologia-hileft.html
technologia-observ.html
technologia-venus-legacy.html
technologia-led-mask.html
akademia.html
akademia 2.html
```

### Assets
```
assets/
  images/
    favicon.svg
    og-preview.svg
    hero/
      hero-clinic-interior.avif
      hero-treatment-room.avif
    clinic/
      clinic-reception.avif
      clinic-consultation-room.avif
    treatments/
      treatment-facial.avif
      treatment-skincare.avif
      treatment-injectable.avif
      treatment-consultation.avif
    technology/
      technology-device.avif
      technology-led.avif
    doctors/
      doctor-portrait.avif
    lifestyle/
      lifestyle-wellness.avif
      lifestyle-pattern.avif
```

### Documentation (10 files)
```
README.md
PRODUCT_STRUCTURE.md
PRODUCT_POSITIONING.md
CMS_STRUCTURE.md
SETUP_GUIDE.md
ONBOARDING_GUIDE.md
DEMO_CONTENT.md
SCREENSHOT_GUIDE.md
PUBLISHING_CHECKLIST.md
LICENSE.txt
```

---

## Files to EXCLUDE from the ZIP

| File/Folder | Reason |
|-------------|--------|
| `TUB-Weboldal-Biblia.html` | Internal design bible (Hungarian) |
| `technologia-OLD-backup.html` | Backup file |
| `névtelen mappa/` | Internal documents and dev tools |
| `.claude/` | IDE/tool configuration |
| `.DS_Store` | macOS system file |
| `ZIP_PACKAGE_GUIDE.md` | This file — internal use only |
| `server.py` | Development utility (if present) |
| `server.sh` | Development utility (if present) |
| Any `.md` files starting with `TUB-` | Internal project documents |

---

## How to Create the ZIP

### macOS Terminal
```bash
cd "/path/to/project/folder"

# Create a clean staging directory
mkdir -p /tmp/aesthetic-clinic-package

# Copy product files
cp the-ultimate-beauty-homepage.html /tmp/aesthetic-clinic-package/
cp kezelesek.html /tmp/aesthetic-clinic-package/
cp konzultacio.html /tmp/aesthetic-clinic-package/
cp protocol.html /tmp/aesthetic-clinic-package/
cp the-ultimate-beauty-protocol.html /tmp/aesthetic-clinic-package/
cp protocol-treatments.html /tmp/aesthetic-clinic-package/
cp protocol-hialuronsav-szinergia.html /tmp/aesthetic-clinic-package/
cp clinical-program.html /tmp/aesthetic-clinic-package/
cp technologia.html /tmp/aesthetic-clinic-package/
cp technologia-hub-new.html /tmp/aesthetic-clinic-package/
cp technologia-hileft.html /tmp/aesthetic-clinic-package/
cp technologia-observ.html /tmp/aesthetic-clinic-package/
cp technologia-venus-legacy.html /tmp/aesthetic-clinic-package/
cp technologia-led-mask.html /tmp/aesthetic-clinic-package/
cp akademia.html /tmp/aesthetic-clinic-package/
cp "akademia 2.html" /tmp/aesthetic-clinic-package/

# Copy assets
cp -r assets /tmp/aesthetic-clinic-package/

# Copy documentation
cp README.md /tmp/aesthetic-clinic-package/
cp PRODUCT_STRUCTURE.md /tmp/aesthetic-clinic-package/
cp PRODUCT_POSITIONING.md /tmp/aesthetic-clinic-package/
cp CMS_STRUCTURE.md /tmp/aesthetic-clinic-package/
cp SETUP_GUIDE.md /tmp/aesthetic-clinic-package/
cp ONBOARDING_GUIDE.md /tmp/aesthetic-clinic-package/
cp DEMO_CONTENT.md /tmp/aesthetic-clinic-package/
cp SCREENSHOT_GUIDE.md /tmp/aesthetic-clinic-package/
cp PUBLISHING_CHECKLIST.md /tmp/aesthetic-clinic-package/
cp LICENSE.txt /tmp/aesthetic-clinic-package/

# Create the ZIP
cd /tmp
zip -r "Aesthetic-Clinic-Website-System-v1.0.zip" aesthetic-clinic-package/

# Clean up
rm -rf /tmp/aesthetic-clinic-package

echo "ZIP created at: /tmp/Aesthetic-Clinic-Website-System-v1.0.zip"
```

---

## ZIP File Naming

Use consistent naming for marketplace uploads:

```
Aesthetic-Clinic-Website-System-v1.0.zip
```

For updates:
```
Aesthetic-Clinic-Website-System-v1.1.zip
Aesthetic-Clinic-Website-System-v2.0.zip
```

---

## Expected ZIP Size

- HTML files (16): ~2-4 MB total (inline CSS/JS)
- Assets: < 100 KB (SVG favicon + OG image)
- Documentation (10): ~100 KB
- **Total estimated**: 3-5 MB

---

## Pre-ZIP Checklist

- [ ] All 16 HTML files included
- [ ] assets/ folder included with favicon and OG image
- [ ] All 10 documentation files included
- [ ] LICENSE.txt included
- [ ] No internal/backup files included
- [ ] No .DS_Store or hidden files included
- [ ] No .claude/ folder included
- [ ] ZIP opens cleanly on both macOS and Windows
- [ ] File names preserved (including spaces in "akademia 2.html")
