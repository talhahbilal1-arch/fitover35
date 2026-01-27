# Fit Over 35 Website

Fitness website for men over 35. Built for deployment on GitHub Pages, Netlify, or any static hosting.

## Quick Start

### Deploy to GitHub Pages

1. Create a new GitHub repository named `fitover35`
2. Push this folder to the repository:
   ```bash
   cd fitover35
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/fitover35.git
   git push -u origin main
   ```
3. Go to repository Settings > Pages
4. Select "Deploy from a branch" > main > / (root)
5. Your site will be live at `https://YOUR_USERNAME.github.io/fitover35`

### Connect Custom Domain

1. In GitHub Pages settings, add `fitover35.com` as custom domain
2. Add DNS records at your domain registrar:
   - A record: `@` -> `185.199.108.153`
   - A record: `@` -> `185.199.109.153`
   - A record: `@` -> `185.199.110.153`
   - A record: `@` -> `185.199.111.153`
   - CNAME record: `www` -> `YOUR_USERNAME.github.io`
3. Wait for DNS propagation (can take up to 48 hours)
4. Enable "Enforce HTTPS" in GitHub Pages settings

## Before Going Live

### 1. Replace ConvertKit Form IDs
Search for `YOUR_FORM_ID` in:
- `index.html` (2 locations: signup section and popup)

Replace with your actual ConvertKit form ID from: https://app.convertkit.com/forms

### 2. Update Affiliate Links
The Amazon affiliate tag is set to `fitover35-20`. Update in:
- `index.html` (gear section)
- Any product articles

### 3. Add Google Analytics (Optional)
Add before `</head>` in all HTML files:
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## File Structure

```
fitover35/
├── index.html          # Main landing page
├── css/
│   └── styles.css      # All styles
├── articles/
│   └── compound-lifts-guide.html  # Sample article
├── CNAME               # Custom domain config
├── robots.txt          # SEO config
└── README.md           # This file
```

## Content to Add

- [ ] More articles (nutrition, workouts, gear reviews)
- [ ] Privacy Policy page
- [ ] Terms of Service page
- [ ] About page
- [ ] Lead magnet PDF

## Pinterest Integration

The site is designed to work with the Fit Over 35 Pinterest automation:
- Pinterest pins link to articles and the homepage
- Email signup captures leads from Pinterest traffic
- Product recommendations use Amazon affiliate links
