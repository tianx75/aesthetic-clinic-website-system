# Aesthetic Clinic Website System — Site Architecture

## Design System

### Typography
- **Display / Headings**: Cormorant Garamond (400, 500, 600, 700)
- **Body / UI**: Montserrat (300, 400, 500, 600, 700)

### Color Palette
| Token | Value | Usage |
|-------|-------|-------|
| `--cream` | `#FAF6F1` | Page backgrounds |
| `--ivory` | `#F5EDE3` | Section backgrounds, cards |
| `--charcoal` | `#2C2C2C` | Primary text |
| `--gold` | `#C9A96E` | Accents, CTAs, highlights |
| `--gold-light` | `#D4B87A` | Hover states |
| `--text-secondary` | `#6B6B6B` | Secondary text |

### Breakpoints
| Breakpoint | Target |
|-----------|--------|
| `> 1024px` | Desktop |
| `681px – 1024px` | Tablet |
| `≤ 680px` | Mobile |

---

## Conversion Logic & Patient Journey

### Primary Conversion Funnel

```
Homepage (Brand Positioning)
  ├── Hero → immediate trust + dual CTA
  ├── Philosophy → emotional connection
  ├── Protocol System → methodology credibility
  ├── Indications Grid → "I have this problem"
  ├── Technology → scientific proof
  ├── Treatments → "this is what I need"
  ├── Testimonials → social proof
  └── CTA Banner → conversion
         ↓
Consultation Page (Conversion)
  ├── Value proposition → why book
  ├── Timeline → what to expect
  ├── Form → capture lead
  └── Contact → alternative paths
```

### Secondary Conversion Paths

```
Treatments Catalog → browse by concern → select treatment → Consultation
Technology Pages → understand the science → trust building → Consultation
Protocol System → understand methodology → confidence → Consultation
Academy → education → authority → Consultation
Clinical Programs → structured solution → commitment → Consultation
```

### Page Roles in the Patient Journey

| Stage | Pages | Goal |
|-------|-------|------|
| **Awareness** | Homepage, Academy | First impression, brand positioning |
| **Consideration** | Treatments, Technology, Protocol | Service discovery, trust building |
| **Decision** | Clinical Programs, Protocol Detail | Confidence, methodology proof |
| **Conversion** | Consultation | Lead capture, booking |
| **Retention** | Academy, Protocol | Education, loyalty |

---

## Page Architecture

### 1. Homepage (`the-ultimate-beauty-homepage.html`)
**Role**: Brand positioning → conversion funnel entry

**Sections** (top to bottom):
1. **Navigation** — Sticky top bar with logo, menu links, CTA button
2. **Hero** — Full-viewport with headline, subtitle, dual CTAs
3. **Intro Strip** — Clinic philosophy statement
4. **Trust Strip** — Credentials, certifications, experience
5. **Differentiator** — Unique methodology positioning
6. **Protocol Modal** — Treatment protocol overlay (JS-driven)
7. **Protocol Strip** — Visual protocol steps (Prepare → Treat → Recover)
8. **Indications Grid** — Treatment concern cards (aging, acne, body, etc.)
9. **Technology Section** — Featured technology with specs
10. **Treatments Grid** — Highlighted treatment cards
11. **Skin Diagnostic Promo** — Diagnostic technology feature
12. **Testimonials** — Client social proof
13. **CTA Banner** — Final conversion push
14. **Footer** — Contact, links, legal

**Conversion elements**: Hero CTAs, Protocol CTA, Indications → Treatments, CTA Banner → Consultation

---

### 2. Treatment Catalog (`kezelesek.html`)
**Role**: Service discovery → treatment selection

**Sections**:
1. Navigation
2. Hero — Page title and description
3. Sticky Filter Bar — Category tabs + search (stays on scroll)
4. Category Dividers — Visual separators between groups
5. Treatment Cards — Grid with name, description, detail link
6. Footer

**Categories**: Medical Aesthetics, NOVA, Biostimulators, Body & Rehab, Surgical, Regeneration

**Interaction pattern**: Filter tabs + real-time search (combined filtering)

---

### 3. Consultation Page (`konzultacio.html`)
**Role**: Lead generation → booking conversion

**Sections**:
1. Navigation
2. Hero — Consultation value proposition
3. Timeline — Step-by-step consultation process visualization
4. Booking Form — Name, email, phone, interest, message
5. Contact Info — Phone, email, address, hours
6. Trust Strip — Reassurance
7. Footer

**Conversion elements**: Form submission (FormSubmit.co, replaceable)

---

### 4. Protocol Pages
**Role**: Methodology proof → trust building → confidence

| Page | Purpose |
|------|---------|
| `protocol.html` | Protocol overview with anchor sections |
| `the-ultimate-beauty-protocol.html` | In-depth protocol breakdown |
| `protocol-treatments.html` | Treatments by protocol phase |
| `protocol-hialuronsav-szinergia.html` | Protocol deep-dive example |
| `clinical-program.html` | Multi-session structured programs |

**Navigation pattern**: Hub page (`protocol.html`) with anchor sections (#filozofia, #pillerek, #treatments, #clinical) + linked detail pages

---

### 5. Technology Pages
**Role**: Scientific credibility → trust building

| Page | Purpose |
|------|---------|
| `technologia.html` | Technology hub with modal overlays |
| `technologia-hub-new.html` | Alternate hub layout |
| `technologia-hileft.html` | NOVA Pro — EMS + photobiomodulation detail |
| `technologia-observ.html` | Skin Diagnostic System detail |
| `technologia-venus-legacy.html` | RF Treatment System detail |
| `technologia-led-mask.html` | LED phototherapy detail |

**Interaction pattern**: Hub page with card-click modals → detail page links

---

### 6. Academy Pages
**Role**: Education → authority building → retention

| Page | Purpose |
|------|---------|
| `akademia.html` | Education hub, training tiers |
| `akademia 2.html` | Alternate academy layout |

---

## CMS Collection Schemas

### Treatments

```json
{
  "name": "Signature Facial Rejuvenation",
  "slug": "signature-facial-rejuvenation",
  "category": "medical-aesthetics",
  "short_description": "A comprehensive facial renewal protocol combining advanced diagnostics with targeted treatments.",
  "full_description": "<p>Multi-phase facial treatment...</p>",
  "duration": "90 min",
  "price_from": 350,
  "image": "treatments/facial-rejuvenation.jpg",
  "protocol_link": "protocol-facial",
  "technology": "nova-pro",
  "is_featured": true
}
```

**Example entries:**

| Name | Category | Duration | Price From |
|------|----------|----------|-----------|
| Signature Facial Rejuvenation | medical-aesthetics | 90 min | $350 |
| NOVA Pro Muscle Activation | nova | 45 min | $250 |
| Collagen Stimulator Program | biostimulators | 60 min | $800 |
| RF Body Contouring | body-rehab | 60 min | $300 |
| Micro-Surgical Eye Refresh | surgical | 120 min | $2,500 |
| LED Recovery Protocol | regeneration | 30 min | $150 |

---

### Doctors

```json
{
  "name": "Dr. Sarah Mitchell",
  "title": "Medical Director — Board Certified Dermatologist",
  "slug": "dr-sarah-mitchell",
  "bio": "<p>With over 15 years of experience in medical aesthetics, Dr. Mitchell combines evidence-based medicine with an artistic eye for natural results.</p>",
  "photo": "team/dr-mitchell.jpg",
  "specializations": ["Facial Rejuvenation", "Injectables", "Laser Therapy"],
  "credentials": ["MD", "FAAD", "Board Certified Dermatology"],
  "is_lead": true
}
```

**Example entries:**

| Name | Title | Specializations |
|------|-------|----------------|
| Dr. Sarah Mitchell | Medical Director | Facial Rejuvenation, Injectables |
| Dr. James Chen | Lead Surgeon | Microsurgery, Eye Rejuvenation |
| Dr. Elena Voss | Technology Director | Device-Based Treatments, RF |

---

### Technologies

```json
{
  "name": "NOVA Pro",
  "slug": "nova-pro",
  "description": "<p>Dual-wavelength EMS and photobiomodulation system for neuromuscular stimulation and tissue regeneration.</p>",
  "specs": [
    {"label": "Stimulation", "value": "EMS"},
    {"label": "Wavelength", "value": "730 + 940nm"},
    {"label": "Spectrum", "value": "5 Spectra"},
    {"label": "Duration", "value": "30–40 min"}
  ],
  "hero_image": "technology/nova-pro-hero.jpg",
  "gallery": ["technology/nova-pro-1.jpg", "technology/nova-pro-2.jpg"],
  "related_treatments": ["signature-facial-rejuvenation", "nova-pro-muscle-activation"]
}
```

**Example entries:**

| Name | Type | Key Spec |
|------|------|----------|
| NOVA Pro | EMS + Photobiomodulation | 730 + 940nm dual wavelength |
| Skin Diagnostic System | Clinical Diagnostics | 8 light modes |
| RF Treatment System | Radiofrequency + PEMF | 1 MHz, 150W |
| LED Mask | Phototherapy | Multi-spectrum LED |

---

### Articles

```json
{
  "title": "Understanding Biostimulators: The Science of Collagen Renewal",
  "slug": "understanding-biostimulators",
  "excerpt": "How next-generation biostimulators activate your body's own collagen production for lasting results.",
  "body": "<p>Biostimulatory treatments represent a paradigm shift...</p>",
  "author": "dr-sarah-mitchell",
  "published_date": "2026-02-15",
  "category": "treatments",
  "featured_image": "articles/biostimulators.jpg",
  "is_published": true
}
```

**Example entries:**

| Title | Category | Author |
|-------|----------|--------|
| Understanding Biostimulators | treatments | Dr. Mitchell |
| The NOVA Pro Advantage | technology | Dr. Voss |
| Preparing Your Skin for Treatment | skincare | Dr. Mitchell |
| Men's Aesthetic Guide | wellness | Dr. Chen |

---

### Case Studies

```json
{
  "title": "Full Facial Rejuvenation — 12 Week Program",
  "slug": "full-facial-rejuvenation-12-week",
  "treatment": "signature-facial-rejuvenation",
  "before_image": "cases/case-001-before.jpg",
  "after_image": "cases/case-001-after.jpg",
  "description": "<p>A comprehensive 12-week protocol combining NOVA Pro preparation, targeted injectables, and LED recovery...</p>",
  "sessions_count": 6,
  "duration_weeks": 12
}
```

**Example entries:**

| Title | Treatment | Sessions | Duration |
|-------|-----------|----------|----------|
| Full Facial Rejuvenation | Signature Facial | 6 | 12 weeks |
| Body Contouring Program | RF Body | 8 | 8 weeks |
| Post-Surgical Recovery | LED Protocol | 4 | 4 weeks |

---

## Shared Components

### Navigation
Present on all pages:
- Logo (left) — `Aesthetic <span>Clinic</span>`
- Menu links: Clinic, Protocol, Treatments, Technology, Academy, Consultation
- CTA button (right): "Consultation →"
- Scroll-aware state change (`.scrolled` class)

### Footer
Present on all pages:
- Clinic name and tagline
- Contact column (email, phone, address, hours)
- Protocol links column
- Treatments links column
- Clinic links column
- Legal bar (Privacy Policy, Terms, Copyright)

### Scroll Reveal Animation
IntersectionObserver pattern with `.reveal` → `.revealed` class transition:
```javascript
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('revealed');
    }
  });
}, { threshold: 0.1 });
```

### Button System
| Class | Usage | Style |
|-------|-------|-------|
| `.btn-primary` | Primary actions | Dark bg, white text |
| `.btn-gold` | High-priority CTAs | Gold bg, ivory text |
| `.btn-ghost` | Secondary actions | Text + underline |
| `.btn-outline-light` | Dark section CTAs | Light border, light text |

---

## Interaction Patterns

### Filter System (Treatment Catalog)
- Category tab buttons with `data-filter` attribute
- Real-time search input with `data-search` matching
- Combined filter + search logic
- Sticky filter bar on scroll
- Empty state messaging

### Modal System (Technology Pages)
- Card click → `openModal(id)` → overlay with `.active` class
- Close via X button, Escape key, or overlay click
- Consistent `.tech-modal-overlay` / `.tech-modal` structure

### Form System (Consultation)
- POST to FormSubmit.co (replaceable)
- Client-side validation
- Select dropdown for treatment interest
- Optional message field

---

## Non-Template Files (Exclude from Product)

| File | Reason |
|------|--------|
| `TUB-PROJEKT-TERV.md` | Internal project plan |
| `TUB-Site-Terkep.html` | Internal sitemap document |
| `TUB-Weboldal-Biblia.html` | Internal design bible |
| `TUB-VENUS-LEGACY-STRATEGIAI-PARTNERSEG.md` | Internal partnership document |
| `technologia-OLD-backup.html` | Backup file |
| `server.py`, `server.sh` | Development utilities |
