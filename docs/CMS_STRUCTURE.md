# Aesthetic Clinic Website System — CMS Structure

This document defines the ideal CMS data model for the Aesthetic Clinic Website System. It is designed for Webflow CMS but adapts to any structured content platform (Sanity, Contentful, Strapi, WordPress ACF, etc.).

---

## Collection: Treatments

**Purpose**: Present clinic services, support filtering, search, and treatment discovery. Powers the treatment catalog page and treatment cards throughout the site.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | Plain Text | Treatment display name |
| Slug | Slug | URL-safe identifier (auto-generated from name) |
| Short Description | Plain Text | 1-2 sentence summary for cards (max 120 chars) |
| Category | Option | `medical-aesthetics`, `nova`, `biostimulators`, `body-rehab`, `surgical`, `regeneration` |
| Hero Image | Image | Primary treatment image (600x400px recommended) |
| Is Featured | Switch | Show on homepage treatments grid |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Full Description | Rich Text | Detailed treatment explanation |
| Treatment Benefits | Rich Text | Bullet list of key benefits |
| Duration | Plain Text | e.g. "45–60 min" |
| Recovery Notes | Plain Text | Expected downtime / aftercare |
| Sessions Recommended | Number | Typical number of sessions |
| Price From | Number | Starting price (display as "From $XXX") |
| CTA Label | Plain Text | Custom button text (default: "Book Consultation") |
| Technology | Reference → Technologies | Related device/technology |
| Protocol Link | Reference → Protocols | Associated protocol page |
| Related Treatments | Multi-Reference → Treatments | Cross-sell suggestions |
| Search Keywords | Plain Text | Additional search terms for filtering |
| Sort Order | Number | Manual sort priority |

### Example Items

| Name | Category | Duration | Price From | Featured |
|------|----------|----------|-----------|----------|
| Signature Facial Rejuvenation | medical-aesthetics | 90 min | $350 | Yes |
| NOVA Pro Muscle Activation | nova | 45 min | $250 | Yes |
| Collagen Stimulator Program | biostimulators | 60 min | $800 | Yes |
| RF Body Contouring | body-rehab | 60 min | $300 | No |
| Micro-Surgical Eye Refresh | surgical | 120 min | $2,500 | No |
| LED Recovery Protocol | regeneration | 30 min | $150 | No |
| Deep Hydration Therapy | medical-aesthetics | 45 min | $200 | No |
| Jawline Definition | nova | 40 min | $350 | Yes |
| Polynucleotide Skin Renewal | biostimulators | 45 min | $600 | No |
| Post-Treatment Recovery | regeneration | 20 min | $100 | No |

---

## Collection: Doctors

**Purpose**: Build trust and authority. Doctor profiles appear on the homepage, team section, and are referenced throughout treatment and technology pages.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | Plain Text | Full name with title (e.g. "Dr. Sarah Mitchell") |
| Slug | Slug | URL-safe identifier |
| Title | Plain Text | Professional title (e.g. "Medical Director") |
| Photo | Image | Professional headshot (800x1000px recommended) |
| Bio | Rich Text | Professional biography |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Specializations | Multi-Select | Areas of expertise |
| Credentials | Plain Text | Degrees and certifications (e.g. "MD, FAAD") |
| Years Experience | Number | Years in practice |
| Education | Rich Text | Medical school, residency, fellowships |
| Publications | Rich Text | Research papers and contributions |
| Is Lead | Switch | Show as primary/lead doctor |
| Sort Order | Number | Display order on team page |
| Consultation Link | URL | Direct booking link for this doctor |
| Languages | Plain Text | Languages spoken |

### Example Items

| Name | Title | Specializations | Lead |
|------|-------|----------------|------|
| Dr. Sarah Mitchell | Medical Director — Board Certified Dermatologist | Facial Rejuvenation, Injectables, Laser Therapy | Yes |
| Dr. James Chen | Lead Surgeon — Oculoplastic Specialist | Microsurgery, Eye Rejuvenation, Facial Contouring | No |
| Dr. Elena Voss | Technology Director — Aesthetic Medicine | Device-Based Treatments, RF Therapy, Photobiomodulation | No |
| Dr. Michael Torres | Associate Physician — Dermatology | Skin Health, Biostimulators, Anti-Aging | No |

---

## Collection: Technologies

**Purpose**: Establish scientific credibility and differentiation. Powers the technology hub pages and modal overlays. Connects to treatments to show which device is used for each service.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | Plain Text | Technology/device display name |
| Slug | Slug | URL-safe identifier |
| Tagline | Plain Text | One-line positioning statement |
| Description | Rich Text | What the technology does and why it matters |
| Hero Image | Image | Device or treatment image (800x600px) |
| Category | Option | `ems`, `rf`, `led`, `diagnostics`, `laser`, `ultrasound` |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Specs | Rich Text | Technical specifications table |
| Mechanism | Rich Text | How the technology works (scientific explanation) |
| Key Benefits | Rich Text | Patient-facing benefit list |
| Clinical Evidence | Rich Text | Studies, certifications, FDA clearances |
| Gallery | Multi-Image | Additional device/treatment photos |
| Related Treatments | Multi-Reference → Treatments | Treatments using this technology |
| Detail Page | URL | Link to dedicated technology page |
| Badge Text | Plain Text | e.g. "FDA Cleared", "Clinically Proven" |
| Sort Order | Number | Display order on tech hub |

### Example Items

| Name | Category | Tagline |
|------|----------|---------|
| NOVA Pro | ems | Dual-wavelength neuromuscular stimulation for deep tissue activation |
| Skin Diagnostic System | diagnostics | Clinical-grade skin analysis across 8 light spectra |
| RF Treatment System | rf | Multipolar radiofrequency with PEMF for contouring and tightening |
| LED Phototherapy Mask | led | Multi-spectrum LED for accelerated tissue recovery |

---

## Collection: Articles

**Purpose**: Support SEO, establish thought leadership, and educate patients. Powers blog/knowledge hub section.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Title | Plain Text | Article headline |
| Slug | Slug | URL-safe identifier |
| Excerpt | Plain Text | 1-2 sentence preview (max 160 chars) |
| Body | Rich Text | Full article content |
| Featured Image | Image | Hero/card image (1200x630px for OG sharing) |
| Category | Option | `skincare`, `treatments`, `technology`, `wellness`, `education` |
| Published Date | Date | Publication date |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Author | Reference → Doctors | Article author |
| Read Time | Number | Estimated minutes to read |
| Related Treatments | Multi-Reference → Treatments | Linked treatments |
| Related Technologies | Multi-Reference → Technologies | Linked devices |
| Tags | Multi-Select | Topic tags for filtering |
| Is Published | Switch | Draft vs. live toggle |
| Is Featured | Switch | Show on homepage/highlights |
| SEO Title | Plain Text | Custom meta title |
| SEO Description | Plain Text | Custom meta description |

### Example Items

| Title | Category | Author | Read Time |
|-------|----------|--------|-----------|
| Understanding Biostimulators: The Science of Collagen Renewal | treatments | Dr. Mitchell | 6 min |
| The NOVA Pro Advantage: Why EMS Changes Everything | technology | Dr. Voss | 8 min |
| Preparing Your Skin for Treatment Season | skincare | Dr. Mitchell | 4 min |
| Men's Aesthetic Guide: What to Expect | wellness | Dr. Chen | 5 min |
| Post-Treatment Recovery: What the Science Says | education | Dr. Torres | 7 min |

---

## Collection: Case Studies

**Purpose**: Visual social proof. Before/after results build patient confidence and demonstrate treatment outcomes.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Title | Plain Text | Case study title |
| Slug | Slug | URL-safe identifier |
| Treatment | Reference → Treatments | Primary treatment used |
| Before Image | Image | Before photo (600x600px, consistent lighting) |
| After Image | Image | After photo (same angle and lighting) |
| Description | Rich Text | Treatment approach and results |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Patient Age Range | Option | `20s`, `30s`, `40s`, `50s`, `60+` |
| Patient Gender | Option | `female`, `male` |
| Sessions Count | Number | Total sessions in program |
| Duration Weeks | Number | Program duration in weeks |
| Technologies Used | Multi-Reference → Technologies | Devices involved |
| Doctor | Reference → Doctors | Treating physician |
| Patient Quote | Plain Text | Testimonial from patient |
| Is Featured | Switch | Show on homepage |
| Consent Given | Switch | GDPR/consent verification |

### Example Items

| Title | Treatment | Sessions | Duration |
|-------|-----------|----------|----------|
| Full Facial Rejuvenation — 12 Week Program | Signature Facial | 6 | 12 weeks |
| Body Contouring Transformation | RF Body Contouring | 8 | 8 weeks |
| Post-Surgical Recovery Protocol | LED Recovery | 4 | 4 weeks |
| Jawline Redefinition — Male Patient | Jawline Definition | 3 | 6 weeks |
| Skin Texture Renewal — 40s | Collagen Stimulator | 4 | 10 weeks |

---

## Collection: Testimonials

**Purpose**: Social proof and emotional trust building. Powers testimonial sections across the site.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Quote | Plain Text | Patient testimonial text |
| Patient Name | Plain Text | First name or initials (e.g. "Sarah M.") |
| Treatment | Reference → Treatments | Treatment received |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Rating | Number | 1-5 star rating |
| Patient Photo | Image | Optional headshot |
| Patient Age | Plain Text | Age or age range |
| Date | Date | When testimonial was given |
| Is Featured | Switch | Show on homepage |
| Source | Option | `in-person`, `google`, `email`, `social` |
| Case Study | Reference → Case Studies | Linked before/after |

### Example Items

| Patient | Quote | Treatment | Rating |
|---------|-------|-----------|--------|
| Sarah M. | "The most thoughtful consultation I've ever experienced. They truly listened." | Signature Facial | 5 |
| David K. | "Professional, discreet, and the results speak for themselves." | Jawline Definition | 5 |
| Emma L. | "I was nervous about my first treatment. The team made me feel completely at ease." | Collagen Stimulator | 5 |
| James R. | "Finally, a clinic that combines real science with genuine care." | NOVA Pro | 5 |

---

## Collection: FAQs

**Purpose**: Address common patient questions, reduce support inquiries, and improve SEO with structured content.

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| Question | Plain Text | The question |
| Answer | Rich Text | Detailed answer |
| Category | Option | `general`, `treatments`, `pricing`, `recovery`, `booking`, `technology` |

### Optional Fields

| Field | Type | Description |
|-------|------|-------------|
| Related Treatment | Reference → Treatments | Specific treatment this FAQ relates to |
| Sort Order | Number | Display priority within category |
| Is Featured | Switch | Show on main FAQ section |

### Example Items

| Question | Category |
|----------|----------|
| How long does a typical consultation take? | booking |
| What should I expect during my first visit? | general |
| How soon will I see results? | treatments |
| Is there any downtime after treatment? | recovery |
| Do you offer payment plans? | pricing |
| How does the NOVA Pro technology work? | technology |

---

## Webflow CMS Implementation Notes

### Collection List Bindings

| Template Section | Collection | Binding |
|-----------------|------------|---------|
| Homepage treatment cards | Treatments | Filter: `is_featured = true`, Limit: 6 |
| Treatment catalog grid | Treatments | All items, sorted by `sort_order` |
| Technology hub cards | Technologies | All items, sorted by `sort_order` |
| Testimonial slider | Testimonials | Filter: `is_featured = true`, Limit: 4 |
| Blog/article listing | Articles | Filter: `is_published = true`, Sort: `published_date desc` |
| Case study gallery | Case Studies | Filter: `is_featured = true` |
| FAQ accordion | FAQs | Group by `category`, sort by `sort_order` |

### Dynamic Page Routes

| Collection | Route Pattern | Template |
|-----------|--------------|---------|
| Treatments | `/treatments/{slug}` | Treatment detail template |
| Doctors | `/team/{slug}` | Doctor profile template |
| Technologies | `/technology/{slug}` | Technology detail template |
| Articles | `/journal/{slug}` | Article template |
| Case Studies | `/results/{slug}` | Case study template |

### Conditional Visibility Rules

- Show "Featured" badge on treatment cards when `is_featured = true`
- Show price when `price_from > 0`
- Show "Sessions" info when `sessions_recommended > 0`
- Show author photo when `author.photo` exists
- Show "Before/After" section when case study has both images
