# Launch Checklist

Step-by-step guide for packaging and publishing the Premium Beauty Clinic Website Template.

---

## 1. Pre-Launch Verification

- [ ] Confirm `FINAL_PROJECT_AUDIT.md` shows READY FOR SALE status
- [ ] Verify all 16 HTML pages open correctly in a browser
- [ ] Verify all 13 AVIF images and 2 SVG files load properly
- [ ] Confirm all 8 screenshots are present in `screenshots/`
- [ ] Confirm all documentation files are present (README.md, SETUP_GUIDE.md, etc.)
- [ ] Confirm `LICENSE.txt` is included and contains correct terms
- [ ] Confirm `TO_REMOVE_BEFORE_SALE/` folder exists and will be excluded from the ZIP
- [ ] Test on multiple browsers (Chrome, Firefox, Safari, Edge)
- [ ] Test responsive layout on mobile and tablet viewports

---

## 2. ZIP Package Preparation

- [ ] Remove or exclude the `TO_REMOVE_BEFORE_SALE/` folder entirely
- [ ] Remove `FINAL_PROJECT_AUDIT.md` and `LAUNCH_CHECKLIST.md` (internal use only)
- [ ] Create ZIP file with a clean product name (e.g., `premium-beauty-clinic-template-v1.0.zip`)
- [ ] Verify ZIP extracts cleanly on macOS and Windows
- [ ] Verify ZIP file size is reasonable (under 50 MB)
- [ ] Open the extracted files in a browser to confirm everything works from the ZIP

---

## 3. Gumroad Upload Steps

1. **Create Product**
   - [ ] Log in to [gumroad.com](https://gumroad.com) and click "New Product"
   - [ ] Select product type: Digital Product

2. **Product Details**
   - [ ] Set product name (use content from `LISTING_TITLE.txt`)
   - [ ] Paste product description (use content from `SHORT_DESCRIPTION.txt` and `PRODUCT_POSITIONING.md`)
   - [ ] Set price: $197 to $297 (recommended: $247 launch price)
   - [ ] Optionally enable "Pay what you want" with a minimum of $197

3. **Upload Files**
   - [ ] Upload the ZIP package as the deliverable file
   - [ ] Upload all 8 screenshots as product gallery images
   - [ ] Upload `og-preview.svg` or a PNG version as the cover image

4. **Configuration**
   - [ ] Set license type (Single Use / Extended License as defined in LICENSE.txt)
   - [ ] Add relevant tags: website template, beauty clinic, aesthetic clinic, HTML template, responsive
   - [ ] Enable PDF receipt
   - [ ] Set a URL-friendly permalink

5. **Publish**
   - [ ] Preview the product listing
   - [ ] Click Publish

---

## 4. Lemon Squeezy Upload Steps

1. **Create Product**
   - [ ] Log in to [lemonsqueezy.com](https://lemonsqueezy.com) and navigate to Products
   - [ ] Click "New Product"

2. **Product Details**
   - [ ] Set product name (use content from `LISTING_TITLE.txt`)
   - [ ] Paste product description (use content from `SHORT_DESCRIPTION.txt` and `PRODUCT_POSITIONING.md`)
   - [ ] Set price: $197 to $297 (recommended: $247 launch price)
   - [ ] Select "Single payment" pricing model

3. **Upload Files**
   - [ ] Upload the ZIP package as the product file
   - [ ] Upload all 8 screenshots to the media gallery
   - [ ] Set a thumbnail / cover image

4. **Configuration**
   - [ ] Set the product category to "Templates" or "Website Templates"
   - [ ] Add tags: website template, beauty clinic, aesthetic, HTML, CSS
   - [ ] Configure license key generation if using license-based distribution
   - [ ] Set up a thank-you page or redirect URL

5. **Publish**
   - [ ] Preview the product store page
   - [ ] Activate the product

---

## 5. Post-Launch Verification

- [ ] Complete a test purchase on each platform (use discount code for $0 or $1)
- [ ] Verify the download link delivers the correct ZIP file
- [ ] Extract the downloaded ZIP and confirm all files are intact
- [ ] Verify the purchase confirmation email arrives with download instructions
- [ ] Check that the product page renders correctly on mobile devices

---

## 6. Promotion

- [ ] Share the product link on social media (Instagram, X/Twitter, LinkedIn)
- [ ] Post in relevant communities (IndieHackers, Product Hunt, design forums)
- [ ] Create a short demo video or GIF walkthrough
- [ ] Reach out to beauty and wellness industry contacts
- [ ] Consider a limited-time launch discount (e.g., 20% off first week)
- [ ] Monitor reviews and respond to buyer questions promptly

---

## 7. Optional: Deploy a Live Demo

Deploying a live demo site increases buyer confidence significantly.

### Netlify

1. [ ] Create a free account at [netlify.com](https://netlify.com)
2. [ ] Drag and drop the project folder (excluding `TO_REMOVE_BEFORE_SALE/`) to Netlify
3. [ ] Set a custom subdomain (e.g., `beauty-clinic-template.netlify.app`)
4. [ ] Add the demo URL to your product listing description

### Vercel

1. [ ] Create a free account at [vercel.com](https://vercel.com)
2. [ ] Import the project as a static site
3. [ ] Configure the build output directory to the project root
4. [ ] Set a custom subdomain and add the demo URL to your product listing

### GitHub Pages

1. [ ] Push the project to a public GitHub repository
2. [ ] Enable GitHub Pages in repository settings (source: main branch)
3. [ ] Add the generated URL to your product listing

---

## Summary

| Step | Platform | Status |
|---|---|---|
| Pre-launch verification | Local | [ ] |
| ZIP package prepared | Local | [ ] |
| Gumroad listing live | Gumroad | [ ] |
| Lemon Squeezy listing live | Lemon Squeezy | [ ] |
| Test purchase completed | Both | [ ] |
| Promotion started | Social / Communities | [ ] |
| Live demo deployed | Netlify / Vercel | [ ] |
