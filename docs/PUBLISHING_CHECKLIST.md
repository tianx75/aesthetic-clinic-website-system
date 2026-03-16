# Aesthetic Clinic Website System — Publishing Checklist

Use this checklist before listing the product on any marketplace.

---

## Content Verification

- [ ] All pages display English demo content (no Hungarian text)
- [ ] No real clinic names, doctor names, or patient names
- [ ] No real email addresses (all show `info@yourclinic.com`)
- [ ] No real phone numbers (all show `+1 (555) 000-0000`)
- [ ] No real addresses (all show generic "City" placeholder)
- [ ] No real brand names (NOVA, NOVA Pro used as generic placeholders)
- [ ] No copyrighted treatment brand names (no Botox, Sculptra, Radiesse, etc.)
- [ ] All demo content is professional and realistic (no lorem ipsum)
- [ ] Footer copyright shows generic "Aesthetic Clinic"
- [ ] Meta tags contain placeholder content, not real clinic data

---

## Image Verification

- [ ] No copyrighted images included
- [ ] No real patient photos
- [ ] No real doctor photos
- [ ] All images are either placeholder blocks, licensed stock, or removed
- [ ] OG/social share images are generic or placeholder
- [ ] Favicon is generic or removed

---

## Navigation & Links

- [ ] All navigation links work on every page
- [ ] No broken internal links (no 404s)
- [ ] Footer links are consistent across all pages
- [ ] Mobile hamburger menu works correctly
- [ ] CTA buttons link to consultation page
- [ ] Logo links back to homepage
- [ ] Scroll-to-section anchors work correctly

---

## Responsive Design

- [ ] Desktop layout verified (1920px, 1440px, 1280px)
- [ ] Tablet layout verified (1024px, 768px)
- [ ] Mobile layout verified (414px, 375px)
- [ ] No horizontal scroll on any viewport
- [ ] Images scale correctly
- [ ] Text remains readable at all sizes
- [ ] Navigation collapses to mobile menu at correct breakpoint
- [ ] Forms are usable on mobile

---

## Interactions & Animations

- [ ] Scroll reveal animations trigger correctly
- [ ] Technology modals open and close properly
- [ ] Modal dismiss via X button, Escape key, and overlay click
- [ ] Treatment filter buttons work
- [ ] Treatment search input works
- [ ] Combined filter + search works correctly
- [ ] Sticky nav changes on scroll
- [ ] No console JavaScript errors

---

## Code Quality

- [ ] All HTML files validate (no critical errors)
- [ ] No inline scripts referencing real APIs or services
- [ ] Form action URLs use placeholder or FormSubmit.co
- [ ] No tracking codes (GA, GTM, Facebook Pixel, etc.)
- [ ] No third-party scripts except Google Fonts
- [ ] CSS custom properties are documented
- [ ] No minified code that can't be read/edited

---

## CMS Readiness

- [ ] `CMS_STRUCTURE.md` defines all collections
- [ ] Collection schemas have required and optional fields
- [ ] Example items provided for each collection
- [ ] Webflow binding recommendations documented
- [ ] Dynamic page routes suggested
- [ ] `data-cat` and `data-filter` attributes are documented

---

## Documentation Package

- [ ] `README.md` — Product overview and customization guide
- [ ] `PRODUCT_STRUCTURE.md` — Site architecture and conversion logic
- [ ] `SETUP_GUIDE.md` — Technical customization reference
- [ ] `ONBOARDING_GUIDE.md` — 48-hour launch guide
- [ ] `CMS_STRUCTURE.md` — CMS collections and schemas
- [ ] `PRODUCT_POSITIONING.md` — Product marketing and positioning
- [ ] `PUBLISHING_CHECKLIST.md` — This file

---

## SEO Readiness

- [ ] Every page has a unique `<title>` tag
- [ ] Every page has a unique `<meta name="description">`
- [ ] OG meta tags present on every page
- [ ] Canonical URLs use placeholder domain
- [ ] `lang="en"` set on all pages
- [ ] Heading hierarchy is correct (single H1 per page)
- [ ] Image alt text is descriptive

---

## Files to EXCLUDE from Product Package

These files must be removed before distribution:

| File | Reason |
|------|--------|
| `TUB-PROJEKT-TERV.md` | Internal project plan (Hungarian) |
| `TUB-Site-Terkep.html` | Internal sitemap (Hungarian) |
| `TUB-Weboldal-Biblia.html` | Internal design bible (Hungarian) |
| `TUB-VENUS-LEGACY-STRATEGIAI-PARTNERSEG.md` | Internal partnership doc (Hungarian) |
| `technologia-OLD-backup.html` | Backup file |
| `server.py` | Development utility |
| `server.sh` | Development utility |
| `.claude/` | IDE configuration folder |
| `.DS_Store` | macOS system file |
| Any `.git` folder | Version control history |

---

## Marketplace-Specific Requirements

### Webflow Marketplace
- [ ] Template imported into Webflow
- [ ] CMS collections created and populated with demo items
- [ ] Interactions and animations working in Webflow
- [ ] Responsive breakpoints configured
- [ ] Preview site published at staging URL
- [ ] Marketplace listing description written
- [ ] Preview screenshots captured (desktop + mobile)
- [ ] Category: "Health & Wellness" or "Business"

### Gumroad
- [ ] Product ZIP file created (excluding internal files)
- [ ] Product description written (use `PRODUCT_POSITIONING.md`)
- [ ] Preview images uploaded (3-5 screenshots)
- [ ] Pricing set ($197-297 range)
- [ ] License terms defined
- [ ] Tags added: aesthetic, clinic, medical, template, website
- [ ] Thank you page / delivery email configured

### Lemon Squeezy
- [ ] Product ZIP file created (excluding internal files)
- [ ] Product description written
- [ ] Preview images uploaded
- [ ] Pricing set with optional variants (Standard / Extended license)
- [ ] License keys configured (if applicable)
- [ ] Digital delivery configured
- [ ] Refund policy defined

---

## Preview & Marketing Assets

- [ ] Full-page desktop screenshot of homepage
- [ ] Full-page mobile screenshot of homepage
- [ ] Treatment catalog page screenshot (showing filters)
- [ ] Technology page screenshot (showing modal interaction)
- [ ] Consultation page screenshot (showing form)
- [ ] Short demo video / GIF showing scroll animations
- [ ] Before/after comparison (generic template vs. this system)
- [ ] Feature list graphic for marketplace listing

---

## Final Sign-Off

- [ ] All checklist items above verified
- [ ] Product tested by someone who didn't build it
- [ ] ZIP file opens cleanly and all files are present
- [ ] Documentation is clear to a first-time reader
- [ ] Pricing reflects the value delivered
- [ ] Ready to publish
