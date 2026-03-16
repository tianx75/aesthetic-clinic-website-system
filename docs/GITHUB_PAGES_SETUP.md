# GitHub Pages Setup

Step-by-step instructions to enable GitHub Pages for the live demo.

---

## Prerequisites

- Repository must be pushed to GitHub first (see `GITHUB_PUBLISHING_STEPS.md`)

---

## Setup Steps

### 1. Open Repository Settings

- Go to your repository on GitHub
- Click the **Settings** tab (gear icon, top right of the repo page)

### 2. Navigate to Pages

- In the left sidebar, scroll down to **Code and automation**
- Click **Pages**

### 3. Configure Source

- Under **Build and deployment**:
  - **Source:** Select **Deploy from a branch**
  - **Branch:** Select **main**
  - **Folder:** Select **/ (root)**
- Click **Save**

### 4. Wait for Deployment

- GitHub will start building the site
- This usually takes 1-3 minutes
- A green checkmark will appear when ready

### 5. Access Your Site

Your site will be available at:

```
https://YOURUSERNAME.github.io/aesthetic-clinic-website-system/
```

The `index.html` in the root automatically redirects to `the-ultimate-beauty-homepage.html`.

---

## Verify Deployment

Check these items after the site is live:

- [ ] Homepage loads correctly
- [ ] All navigation links work
- [ ] Images load (AVIF format)
- [ ] Favicon appears in browser tab
- [ ] Scroll animations play
- [ ] Treatment catalog filter works
- [ ] Mobile layout works (resize browser or use DevTools)

---

## Custom Domain (Optional)

If you want to use a custom domain for the demo:

1. In **Pages** settings, enter your domain under **Custom domain**
2. Add a CNAME record in your DNS pointing to `YOURUSERNAME.github.io`
3. Check **Enforce HTTPS**
4. Wait for DNS propagation (up to 24 hours)

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| 404 error | Verify branch is `main` and folder is `/ (root)` |
| Images not loading | Check browser supports AVIF (Chrome, Firefox, Edge do) |
| CSS not loading | All CSS is inline, should work immediately |
| Old version showing | Hard refresh with Ctrl+Shift+R or wait for cache to clear |
