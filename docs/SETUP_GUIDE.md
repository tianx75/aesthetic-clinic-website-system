# Aesthetic Clinic Website System — Setup Guide

Launch your premium aesthetic clinic website in 48 hours.

---

## Step 1: Import Template

### Option A — Static HTML
1. Download and extract the template files
2. Upload to your hosting provider (Netlify, Vercel, or any static host)
3. Point your domain to the hosting

### Option B — Webflow
1. Import the template into your Webflow workspace
2. The design system, animations, and interactions will carry over
3. Connect your custom domain in Webflow Settings → Hosting

### Option C — Other CMS
1. Use the HTML files as reference for structure
2. Recreate the design system using the CSS custom properties in `:root`
3. Map the CMS collections (see Step 3)

---

## Step 2: Replace Brand Name

Search and replace these placeholders across all pages:

| Find | Replace With |
|------|-------------|
| `Aesthetic Clinic` | Your clinic name |
| `Aesthetic <span>Clinic</span>` | Your Name `<span>`Styled Word`</span>` |
| `info@yourclinic.com` | Your email |
| `+1 (555) 000-0000` | Your phone number |
| `City` | Your city name |
| `123 Clinic Avenue, City, ST 00000` | Your address |
| `yourclinic.com` | Your domain (in meta tags) |

### Brand Color Customization

Update the CSS custom properties in each file's `:root` block:

```css
:root {
  --cream: #FAF6F1;      /* Page backgrounds */
  --ivory: #F5EDE3;      /* Card/section backgrounds */
  --charcoal: #2C2C2C;   /* Primary text */
  --gold: #C9A96E;       /* Accent color — change this to your brand color */
  --gold-light: #D4B87A; /* Hover state — lighter version of your accent */
}
```

---

## Step 3: Add Treatments

### Treatment Catalog (`kezelesek.html`)

Each treatment is a card in the grid. To add a new treatment:

```html
<div class="treat-card" data-cat="your-category" data-search="treatment name keywords">
  <div class="treat-card__img">
    <img src="assets/images/treatment-name.jpg" alt="Treatment Name">
  </div>
  <div class="treat-card__body">
    <span class="treat-card__tag">Category Name</span>
    <h3 class="treat-card__title">Treatment Name</h3>
    <p class="treat-card__desc">Brief description of the treatment and expected results.</p>
    <a href="treatment-detail.html" class="treat-card__link">Details →</a>
  </div>
</div>
```

### Filter Categories

Update filter buttons to match your treatment categories:

```html
<button class="fbtn active" data-filter="all">All</button>
<button class="fbtn" data-filter="injectables">Injectables</button>
<button class="fbtn" data-filter="laser">Laser</button>
<button class="fbtn" data-filter="body">Body</button>
<!-- Add your categories -->
```

The `data-filter` value must match the `data-cat` value on treatment cards.

---

## Step 4: Add Doctor Profiles

Doctor information appears on the homepage and can be expanded to a dedicated team page.

For each doctor, prepare:
- Professional headshot (recommended: 800x1000px, neutral background)
- Full name and title (e.g., "Dr. Jane Smith, MD, FAACS")
- Specializations list
- Short bio (2-3 sentences)
- Credentials and certifications

### Homepage Doctor Section

```html
<div class="doctor-card">
  <img src="assets/images/doctor-name.jpg" alt="Dr. Name" class="doctor-card__photo">
  <h3 class="doctor-card__name">Dr. Jane Smith</h3>
  <p class="doctor-card__title">Medical Director — Board Certified Dermatologist</p>
  <p class="doctor-card__bio">Brief professional biography highlighting expertise and approach.</p>
</div>
```

---

## Step 5: Replace Images

### Image Specifications

| Location | Recommended Size | Format | Notes |
|----------|-----------------|--------|-------|
| Hero backgrounds | 1920x1080px | JPG/WebP | Compress to < 300KB |
| Treatment cards | 600x400px | JPG/WebP | Consistent aspect ratio |
| Doctor photos | 800x1000px | JPG/WebP | Neutral background |
| Technology images | 800x600px | JPG/WebP | Product/device photos |
| Before/After | 600x600px | JPG | Same lighting & angle |
| OG/Social share | 1200x630px | JPG | Used in meta tags |

### Image Optimization
- Use WebP format where possible for faster loading
- Compress all images (TinyPNG, Squoosh, or ImageOptim)
- Add descriptive `alt` text for accessibility and SEO
- Use `loading="lazy"` for below-the-fold images

---

## Step 6: Connect Booking System

### Option A — FormSubmit (Default)

The consultation form is pre-configured with FormSubmit.co. Update the email:

```html
<form action="https://formsubmit.co/your@email.com" method="POST">
```

### Option B — Calendly / Acuity

Replace the form section with an embed:

```html
<div class="booking-embed">
  <iframe src="https://calendly.com/your-clinic/consultation"
          width="100%" height="700" frameborder="0"></iframe>
</div>
```

### Option C — Custom Booking API

Update the form to POST to your booking endpoint:

```html
<form action="https://api.yourbookingsystem.com/appointments" method="POST">
```

### Option D — WhatsApp / Direct Contact

Replace the form with a direct contact CTA:

```html
<a href="https://wa.me/15550000000?text=I'd%20like%20to%20book%20a%20consultation"
   class="btn-gold">Book via WhatsApp →</a>
```

---

## Quick Launch Checklist

- [ ] Template imported and hosted
- [ ] Brand name replaced on all pages
- [ ] Contact info updated (email, phone, address)
- [ ] Logo replaced in navigation and footer
- [ ] Hero images replaced
- [ ] Treatment catalog updated with your services
- [ ] Doctor profiles added
- [ ] Technology pages customized for your devices
- [ ] Consultation form connected to your email/booking system
- [ ] Meta tags updated (title, description, OG images)
- [ ] Favicon uploaded
- [ ] Google Analytics / tracking added
- [ ] Domain connected and SSL active
- [ ] Mobile responsiveness verified
- [ ] All links tested

---

## Post-Launch Recommendations

1. **SEO**: Update meta descriptions on every page with your location and specialties
2. **Analytics**: Add Google Analytics 4 or Plausible tracking script
3. **Speed**: Run Google PageSpeed Insights and optimize any flagged images
4. **Legal**: Add your privacy policy and terms of service content
5. **Schema**: Add LocalBusiness structured data for Google Maps visibility
6. **Reviews**: Connect Google Reviews widget to build social proof
