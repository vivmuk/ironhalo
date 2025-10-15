# Quick Deployment Guide for The Iron Halo Website

## ✅ Pre-Deployment Checklist

Before deploying, ensure:
- [ ] All images are in the same directory as `index.html`
- [ ] Author bio is finalized and accurate
- [ ] Sample chapter text is approved
- [ ] Book purchase links are ready (or using search links as placeholders)
- [ ] Contact form integration is set up (optional)

## 🚀 Deployment Options

### Option 1: GitHub Pages (Recommended - Free & Easy)

**Step 1: Create Repository**
```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: The Iron Halo website"
```

**Step 2: Push to GitHub**
```bash
# Create a new repository on GitHub (via web interface)
# Then link and push:
git remote add origin https://github.com/yourusername/iron-halo.git
git branch -M main
git push -u origin main
```

**Step 3: Enable GitHub Pages**
1. Go to repository Settings
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click "Save"
6. Your site will be live at: `https://yourusername.github.io/iron-halo/`

**Optional: Custom Domain**
1. In GitHub Pages settings, add your custom domain
2. Create a CNAME file in your repository with your domain
3. Configure DNS with your domain registrar:
   - Add CNAME record pointing to `yourusername.github.io`
   - Wait for DNS propagation (can take 24-48 hours)

---

### Option 2: Netlify (Instant Deployment)

**Method A: Drag & Drop**
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag the entire project folder
3. Site goes live instantly with a random URL
4. Claim the site to customize URL or add custom domain

**Method B: Git Integration**
1. Push your code to GitHub (see Option 1, Steps 1-2)
2. Log into [Netlify](https://app.netlify.com/)
3. Click "New site from Git"
4. Connect your GitHub repository
5. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or `.`)
6. Click "Deploy site"

**Netlify Features:**
- Free HTTPS
- Auto-deploys on git push
- Form handling (no backend needed)
- Serverless functions support

**Configure Netlify Forms:**
Update the contact form in `index.html`:
```html
<form name="contact" method="POST" data-netlify="true" netlify-honeypot="bot-field">
  <input type="hidden" name="form-name" value="contact" />
  <!-- your existing form fields -->
</form>
```

---

### Option 3: Vercel (Fast & Developer-Friendly)

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy from project directory:
```bash
vercel
```

3. Follow prompts and your site goes live instantly

---

### Option 4: Traditional Web Hosting

**Upload via FTP/SFTP:**

1. Get hosting credentials from your provider
2. Use an FTP client (FileZilla, Cyberduck, etc.)
3. Upload all files to `public_html` or `www` directory
4. Ensure `index.html` is in the root
5. Visit your domain

**Popular hosting providers:**
- Bluehost
- SiteGround  
- DreamHost
- HostGator

---

## 🔧 Post-Deployment Configuration

### 1. Update Purchase Links
Once the book is published with confirmed ISBNs/ASINs:

```html
<!-- Amazon -->
<a href="https://www.amazon.com/dp/YOUR-ASIN-HERE">

<!-- Bookshop -->
<a href="https://bookshop.org/books/the-iron-halo-isbn-here/ISBN">

<!-- Barnes & Noble -->
<a href="https://www.barnesandnoble.com/w/the-iron-halo/BN-ID">
```

### 2. Set Up Contact Form Backend

**Using Formspree (Free):**
1. Sign up at [Formspree.io](https://formspree.io/)
2. Create a new form and get your endpoint
3. Update the form in `index.html`:
```html
<form id="contactForm" action="https://formspree.io/f/YOUR-FORM-ID" method="POST">
```

**Using Netlify Forms:**
Add these attributes to your form tag:
```html
<form name="contact" method="POST" data-netlify="true">
```

### 3. Add Analytics (Optional)

**Google Analytics:**
Add before closing `</head>` tag:
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

**Plausible Analytics (Privacy-Friendly):**
```html
<script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>
```

### 4. Set Up Social Media Preview

Add Open Graph tags in the `<head>`:
```html
<meta property="og:title" content="The Iron Halo — Spandan Shah" />
<meta property="og:description" content="A siege at dusk. A city that remembers. An inventor torn between legacy and ruin." />
<meta property="og:image" content="https://yourdomain.com/Gemini_Generated_Image_46gduv46gduv46gd (1).png" />
<meta property="og:url" content="https://yourdomain.com" />
<meta name="twitter:card" content="summary_large_image" />
```

---

## 🎯 SEO Optimization

### 1. Create sitemap.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yourdomain.com/</loc>
    <lastmod>2025-10-15</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

### 2. Create robots.txt
```
User-agent: *
Allow: /

Sitemap: https://yourdomain.com/sitemap.xml
```

### 3. Submit to Search Engines
- [Google Search Console](https://search.google.com/search-console)
- [Bing Webmaster Tools](https://www.bing.com/webmasters)

---

## 📊 Performance Testing

After deployment, test your site:

1. **Google PageSpeed Insights**
   - https://pagespeed.web.dev/
   - Test both mobile and desktop

2. **WebPageTest**
   - https://www.webpagetest.org/
   - Test from multiple locations

3. **GTmetrix**
   - https://gtmetrix.com/
   - Get detailed performance reports

---

## 🔒 Security & Best Practices

### Enable HTTPS
All modern hosting platforms provide free SSL certificates. Ensure HTTPS is enabled:
- GitHub Pages: Automatic
- Netlify: Automatic
- Vercel: Automatic
- Traditional hosting: Use Let's Encrypt

### Content Security Policy (Optional)
Add to `<head>`:
```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self' https://cdn.tailwindcss.com; script-src 'self' 'unsafe-inline' https://cdn.tailwindcss.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;">
```

---

## 📱 Mobile Testing

Test on real devices:
- iOS Safari
- Android Chrome
- Different screen sizes

Use browser DevTools device emulation for quick testing.

---

## 🆘 Troubleshooting

### Images not loading
- Check file paths are relative (no leading `/`)
- Verify image filenames match exactly (case-sensitive)
- Ensure images are uploaded to same directory as HTML

### Forms not working
- Netlify: Ensure form attributes are correct
- Formspree: Check endpoint URL
- Test with simple alert first, then integrate backend

### Audio not playing
- WebAudio API requires user interaction (button click)
- Some browsers require HTTPS for audio
- Check browser console for errors

### Animations not smooth
- Ensure hardware acceleration is enabled
- Test on different devices
- Consider reducing particle count on mobile

---

## 📈 Marketing & Launch

1. **Pre-launch checklist:**
   - [ ] Test all links
   - [ ] Verify mobile responsiveness
   - [ ] Check all images load
   - [ ] Test contact form
   - [ ] Proofread all text

2. **Announce launch:**
   - Share on social media
   - Email book clubs and reviewers
   - Submit to book-related directories
   - Reach out to literary blogs

3. **Monitor:**
   - Set up analytics
   - Track conversion rates
   - Monitor contact form submissions

---

## 🎉 You're Ready!

Your website is production-ready and includes:
- ✅ Beautiful, immersive design
- ✅ All 10 concept images + author photo
- ✅ Interactive elements
- ✅ E-commerce links
- ✅ Contact form
- ✅ Mobile responsive
- ✅ SEO optimized

Choose your deployment method above and launch your book website today!

---

**Questions?** Refer to the README.md for additional information or consult your hosting provider's documentation.

