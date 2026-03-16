# GitHub Publishing Steps

Exact commands to publish this repository to GitHub.

---

## Option A: Using GitHub CLI (Recommended)

### 1. Install GitHub CLI

```bash
brew install gh
```

### 2. Authenticate

```bash
gh auth login
```

Follow the prompts to authenticate via browser.

### 3. Create Repository and Push

```bash
cd "/Users/theultimatebeautykrisztian/Documents/TUB/1.0 TUB site"

# Create a new GitHub repository (public or private)
gh repo create aesthetic-clinic-website-system --public --source=. --remote=origin --push

# Or for private:
gh repo create aesthetic-clinic-website-system --private --source=. --remote=origin --push
```

### 4. Enable GitHub Pages

```bash
gh api repos/{owner}/aesthetic-clinic-website-system/pages \
  -X POST \
  -f "source[branch]=main" \
  -f "source[path]=/"
```

---

## Option B: Manual (GitHub Web Interface)

### 1. Create Repository on GitHub

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `aesthetic-clinic-website-system`
3. Description: `Premium 16-page website template for medical aesthetics clinics`
4. Choose **Public** or **Private**
5. Do NOT initialize with README (you already have one)
6. Click **Create repository**

### 2. Push Local Repository

Copy and run the commands shown on the new repository page:

```bash
cd "/Users/theultimatebeautykrisztian/Documents/TUB/1.0 TUB site"

git remote add origin https://github.com/YOURUSERNAME/aesthetic-clinic-website-system.git
git push -u origin main
```

Replace `YOURUSERNAME` with your actual GitHub username.

### 3. Verify

- Visit your repository page on GitHub
- Confirm all files are visible
- Check that README.md renders with screenshots

---

## After Publishing

1. Enable GitHub Pages (see `GITHUB_PAGES_SETUP.md`)
2. Update the README.md demo URL with your actual GitHub Pages URL
3. Optionally add repository topics: `website-template`, `aesthetic-clinic`, `medical-website`, `html-css-js`
