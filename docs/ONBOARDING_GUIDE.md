# How to Launch Your Clinic Website in 48 Hours

A step-by-step onboarding guide for the Aesthetic Clinic Website System.

---

## Before You Begin

You will need:
- Your clinic name and tagline
- Logo file (SVG or PNG, light and dark versions)
- 10-15 high-quality photos (hero images, team, clinic interior)
- List of treatments with descriptions
- Doctor profiles with headshots
- Contact information (phone, email, address, hours)
- Booking system URL (Calendly, Acuity, or custom)

---

## Hour 1-4: Identity Setup

### Step 1 — Import the Template

**For Static Hosting (Netlify, Vercel, etc.):**
1. Download and extract the template package
2. Connect to your hosting provider
3. Deploy the folder as a static site

**For Webflow:**
1. Import the template into your Webflow workspace
2. Design system, interactions, and animations will carry over
3. Set up CMS collections per `CMS_STRUCTURE.md`

### Step 2 — Replace Clinic Name and Brand

Open each HTML file and find-replace these placeholders:

| Find This | Replace With |
|-----------|-------------|
| `Aesthetic Clinic` | Your clinic name |
| `Aesthetic <span>Clinic</span>` | Your Name `<span>Styled</span>` |
| `info@yourclinic.com` | Your actual email |
| `+1 (555) 000-0000` | Your actual phone |
| `City` | Your city name |
| `123 Clinic Avenue, City, ST 00000` | Your full address |
| `yourclinic.com` | Your domain |

**Pro tip**: Use a code editor's "Find and Replace in Files" feature to update all pages at once (VS Code: `Cmd+Shift+H`).

### Step 3 — Update Brand Colors (Optional)

If your brand uses different colors, update the `:root` CSS variables in each file:

```css
:root {
  --gold: #C9A96E;      /* → Your primary accent color */
  --gold-light: #D4B87A; /* → Lighter version for hover states */
}
```

The gold accent appears on buttons, links, highlights, and decorative elements. Change these two values to match your brand.

---

## Hour 4-12: Content Setup

### Step 4 — Add Your Treatments

Open `kezelesek.html` (treatment catalog page).

For each treatment card, update:
- Treatment name
- Category tag
- Short description
- Detail page link
- `data-cat` attribute (must match your filter buttons)
- `data-search` attribute (keywords for search functionality)

**Categories to customize:**
Update the filter buttons at the top of the page. The `data-filter` value must match the `data-cat` value on cards.

```html
<button class="fbtn" data-filter="injectables">Injectables</button>
```

### Step 5 — Add Doctor Profiles

Doctor information appears in:
- Homepage team/trust section
- Footer (optionally)
- Protocol pages (methodology attribution)

For each doctor, update:
- Full name and professional title
- Professional headshot (800x1000px)
- Short bio (2-3 sentences)
- Specializations
- Credentials

### Step 6 — Update Technology Pages

You have 4 technology detail pages. For each device your clinic uses:
1. Update the device name, description, and specifications
2. Replace device images
3. Update the mechanism of action explanation
4. Link to relevant treatments

If you don't use all 4 technologies, you can:
- Remove unused technology pages
- Update the technology hub to show only your devices
- Remove links to unused tech pages from navigation and footer

---

## Hour 12-24: Media & Forms

### Step 7 — Replace Images

| Image Location | What to Replace | Recommended Size |
|---------------|----------------|-----------------|
| Hero sections | Clinic lifestyle photos | 1920x1080px |
| Treatment cards | Treatment/result photos | 600x400px |
| Doctor photos | Professional headshots | 800x1000px |
| Technology pages | Device/procedure photos | 800x600px |
| OG meta images | Social sharing images | 1200x630px |
| Favicon | Your logo icon | 32x32px + 180x180px |

**Image tips:**
- Use WebP format for faster loading
- Compress all images (< 300KB for heroes, < 100KB for cards)
- Keep consistent lighting and color grading across photos
- Add descriptive `alt` text for SEO and accessibility

### Step 8 — Connect Booking / Contact Forms

The consultation page (`konzultacio.html`) has a built-in form.

**Option A — FormSubmit (Simplest)**
Update the form action email:
```html
<form action="https://formsubmit.co/your@email.com" method="POST">
```

**Option B — Calendly / Acuity**
Replace the form with a booking widget embed.

**Option C — Custom API**
Update the form action to your booking system endpoint.

**Update CTA buttons across all pages:**
Search for consultation/booking links and ensure they point to your preferred booking method.

---

## Hour 24-36: SEO & Legal

### Step 9 — Update SEO Metadata

In every HTML file, update the `<head>` section:

```html
<title>Your Clinic Name — Premium Medical Aesthetics · Your City</title>
<meta name="description" content="Your unique value proposition in 155 characters.">
<meta property="og:title" content="Your Clinic Name — Premium Medical Aesthetics">
<meta property="og:description" content="Your clinic description for social sharing.">
<meta property="og:url" content="https://yourdomain.com/page">
<meta property="og:image" content="https://yourdomain.com/assets/og-image.jpg">
<link rel="canonical" href="https://yourdomain.com/page">
```

**SEO checklist for each page:**
- [ ] Unique title tag (include city name for local SEO)
- [ ] Unique meta description (include target keywords)
- [ ] OG image specific to the page
- [ ] Canonical URL set correctly
- [ ] H1 tag is unique and descriptive

### Step 10 — Add Legal Pages

The footer links to Privacy Policy and Terms pages. Create these pages with your legal content:
- Privacy Policy (required by GDPR, CCPA)
- Terms of Service
- Cookie Policy (if applicable)

**For medical clinics also consider:**
- Patient consent information
- Before/after photo usage policy
- Telehealth disclaimers (if applicable)

---

## Hour 36-48: Final Review

### Step 11 — Test Everything

**Navigation test:**
- [ ] Click every navigation link on every page
- [ ] Verify all footer links work
- [ ] Test mobile hamburger menu
- [ ] Test scroll-to-section anchors

**Responsive test:**
- [ ] Desktop (1920px, 1440px, 1280px)
- [ ] Tablet (1024px, 768px)
- [ ] Mobile (414px, 375px, 320px)

**Content test:**
- [ ] No placeholder text remaining ("Clinic Name", "Doctor Name", etc.)
- [ ] All images replaced with real photos
- [ ] Contact information is correct
- [ ] Form submissions arrive at correct email

**Performance test:**
- [ ] Run Google PageSpeed Insights
- [ ] All images optimized and compressed
- [ ] No 404 errors in browser console
- [ ] Page loads under 3 seconds on 4G

### Step 12 — Publish

1. Connect your custom domain
2. Enable SSL certificate
3. Set up 301 redirects if migrating from old site
4. Submit sitemap to Google Search Console
5. Test live site one final time
6. Announce launch

---

## Post-Launch (Week 1)

- [ ] Set up Google Analytics 4
- [ ] Add Google Business Profile link
- [ ] Submit to Google Maps
- [ ] Add LocalBusiness schema markup
- [ ] Set up appointment reminder emails
- [ ] Create social media profiles linked from site
- [ ] Start collecting patient testimonials
- [ ] Schedule first blog article

---

## Need Help?

If you need assistance with customization:
- Check `README.md` for technical documentation
- Check `PRODUCT_STRUCTURE.md` for site architecture details
- Check `CMS_STRUCTURE.md` for CMS collection setup
- Check `SETUP_GUIDE.md` for detailed customization reference
