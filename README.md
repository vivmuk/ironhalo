# The Iron Halo - Official Book Website

A beautiful, immersive website for *The Iron Halo* by Spandan Shah, featuring stunning artwork, interactive elements, and seamless e-commerce integration.

## 🌟 Features

### Visual Experience
- **Hero Section**: Dramatic parallax background featuring "The Coming Storm" 
- **Image Gallery**: All 10 concept images strategically placed throughout the site
- **Author Portrait**: Professional author photo in the About section
- **Smooth Animations**: Scroll-based reveal effects and hover interactions
- **Responsive Design**: Fully optimized for mobile, tablet, and desktop

### Interactive Elements
- **Deploy the Halo**: Click to trigger particle effects and immersive audio
- **Hope/Fear Theme Toggle**: Switch between two color palettes representing the book's dual themes
- **Expandable Sample Chapters**: Read excerpts with smooth accordion functionality
- **Contact Form**: Built-in form for press inquiries and reader outreach

### E-Commerce Integration
The website includes direct buy links to:
- **Amazon** - Paperback, Hardcover, and Kindle editions
- **Bookshop.org** - Support independent bookstores
- **Barnes & Noble** - In-store and online availability

## 📁 Project Structure

```
Iron Halo/
├── index.html                                    # Main website file
├── README.md                                     # This file
├── Gemini_Generated_Image_njvyswnjvyswnjvy.png  # Author portrait
├── Gemini_Generated_Image_46gduv46gduv46gd.png  # The Creator's Dilemma
├── Gemini_Generated_Image_46gduv46gduv46gd (1).png  # The Two Cranes
├── Gemini_Generated_Image_46gduv46gduv46gd (2).png  # The Coming Storm
├── Gemini_Generated_Image_46gduv46gduv46gd (3).png  # The Halo's Scar
├── Gemini_Generated_Image_46gduv46gduv46gd (4).png  # The Grove of Whispers
├── Gemini_Generated_Image_c8sw48c8sw48c8sw.png      # The Inventor's Retreat
├── Gemini_Generated_Image_c8sw48c8sw48c8sw (1).png  # The Whispering Walls
├── Gemini_Generated_Image_c8sw48c8sw48c8sw (2).png  # The Silent Vigil
├── Gemini_Generated_Image_c8sw48c8sw48c8sw (3).png  # The Shadowed Path
└── Gemini_Generated_Image_c8sw48c8sw48c8sw (4).png  # The Broken Seal
```

## 🎨 Image Mapping

Each concept image is strategically placed to enhance storytelling:

1. **The Creator's Dilemma** - Featured in Origin/About section
2. **The Two Cranes** - Highlighted as a centerpiece (Hope vs. Fear theme)
3. **The Coming Storm** - Hero background and parallax sections
4. **The Halo's Scar** - Visual gallery and themes section background
5. **The Grove of Whispers** - Visual gallery (espionage theme)
6. **The Inventor's Retreat** - Visual gallery (isolation and genius)
7. **The Whispering Walls** - Visual gallery (ancient secrets)
8. **The Silent Vigil** - Visual gallery (foreboding atmosphere)
9. **The Shadowed Path** - Visual gallery (intrigue and danger)
10. **The Broken Seal** - Visual gallery centerpiece (betrayal theme)
11. **Author Portrait** - About the Author section

## 🚀 Getting Started

### Option 1: Open Locally
Simply double-click `index.html` to open the website in your default browser.

### Option 2: Use a Local Server
For best performance with all features:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## 🌐 Deployment

### GitHub Pages (Free)
1. Create a GitHub repository
2. Push all files (including images) to the repository
3. Go to Settings > Pages
4. Select "Deploy from branch" and choose your main branch
5. Your site will be live at `https://yourusername.github.io/repository-name/`

### Netlify (Free)
1. Drag and drop the entire folder to [Netlify Drop](https://app.netlify.com/drop)
2. Your site will be live instantly with a custom URL

### Custom Domain
Both GitHub Pages and Netlify support custom domain configuration.

## 🛠️ Customization

### Update Buy Links
When the book is published, update the direct product links in the `#buy` section:

```html
<!-- Replace search URLs with direct product pages -->
<a href="https://www.amazon.com/dp/YOUR-ASIN">Amazon</a>
<a href="https://bookshop.org/books/your-book-isbn">Bookshop.org</a>
```

### Modify Author Bio
Edit the text in the `#author` section to match your preferred biography.

### Add More Sample Chapters
Duplicate the `<details>` elements in the `#sample` section to add more excerpts.

### Contact Form Integration
The contact form currently shows a simple confirmation message. For production, integrate with:
- [Formspree](https://formspree.io/) - Simple form backend
- [Netlify Forms](https://www.netlify.com/products/forms/) - Built-in if using Netlify
- [EmailJS](https://www.emailjs.com/) - Send emails directly from JavaScript

## 🎭 Theme System

The site features a dual-theme system reflecting the book's Hope vs. Fear motif:

- **Hope Mode** (Default): Amber/gold accents, warm tones
- **Fear Mode**: Red accents, cool tones, increased saturation

Toggle between themes using the button in the header.

## 📱 Mobile Responsive

The site is fully responsive with:
- Collapsible mobile navigation menu
- Touch-optimized interactive elements
- Optimized image loading
- Smooth scrolling on all devices

## 🔊 Audio Features

The "Deploy the Halo" button triggers:
- Low-frequency buzz rising to a sharp tone (WebAudio API)
- 120 particle spark effects with physics
- Visual feedback with state management

## ⚡ Performance

- **CDN**: Tailwind CSS loaded from CDN for fast delivery
- **Optimized Images**: All images are already optimized PNGs
- **Lazy Loading**: Images load as needed during scroll
- **Smooth Animations**: Hardware-accelerated CSS transforms

## 📝 SEO & Meta Tags

The site includes:
- Descriptive title and meta description
- Semantic HTML structure
- Accessible navigation
- Custom favicon (SVG icon in the header)

## 🎨 Design Philosophy

The website design reflects the book's themes:
- **Medieval meets modern**: Glass morphism with period-appropriate imagery
- **Light and shadow**: High contrast, chiaroscuro-inspired visuals
- **Texture-rich**: Emphasizing materials (iron, paper, stone)
- **Symbolic depth**: Each image tells part of the story without spoilers

## 📧 Support

For technical issues or questions about the website, refer to the contact form or email the author directly.

## 📜 License

All images and content © Spandan Shah. All rights reserved.

---

**Built with care for storytellers and readers alike.**

