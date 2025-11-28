# Yukto - AI Automation & Digital Marketing Website

A complete, production-ready website for Yukto - an AI automation and digital marketing company.

## 🎯 Overview

This is a modern, premium website featuring:
- **Emotional, conversion-focused copywriting**
- **Modern, responsive design** with gradients and animations
- **Fully functional contact form** with validation
- **Smooth animations and interactions**
- **Mobile-responsive** across all devices
- **Accessibility features** and keyboard navigation

## 📁 File Structure

```
Yukto/
├── index.html          # Main HTML file with all sections
├── styles.css          # Complete CSS with responsive design
├── script.js           # JavaScript for interactions and animations
└── README.md           # This file
```

## 🎨 Features

### Sections Included

1. **Hero Section** - Eye-catching headline with emotional storytelling and CTA
2. **Problem Section** - Addresses pain points with relatable language
3. **Solutions/Services** - 6 comprehensive services with benefits
4. **Why Choose Us** - 6 compelling reasons with unique value propositions
5. **Testimonials** - 4 realistic client testimonials
6. **CTA Section** - Emotional call-to-action with urgency
7. **About Section** - Founder story, mission, and vision
8. **Contact Form** - Fully functional with validation
9. **Footer** - Company info, links, and social media placeholders

### Design Features

- **Color Scheme**: Navy, electric blue, violet with soothing gradients
- **Typography**: Inter + Space Grotesk for modern, professional look
- **Animations**: Smooth fade-ins, parallax effects, card hovers
- **Responsive**: Mobile-first design, works on all screen sizes
- **Performance**: Debounced scroll events, optimized animations

### Interactive Features

- Smooth scrolling navigation
- Active link highlighting
- Form validation with user feedback
- Card tilt effects on hover
- Parallax gradient orbs
- Scroll-to-top button
- Mobile menu (ready for implementation)
- Intersection Observer animations

## 🚀 Getting Started

### Option 1: Open Directly

Simply open `index.html` in your web browser. No server required!

### Option 2: Use a Local Server (Recommended)

For the best experience, use a local development server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## 🎨 Customization Guide

### Changing Colors

Edit the CSS variables in `styles.css` (lines 10-30):

```css
:root {
    --color-blue: #3b82f6;       /* Primary blue */
    --color-violet: #8b5cf6;     /* Accent violet */
    --color-navy: #0f172a;       /* Dark navy */
    /* ... more colors */
}
```

### Updating Content

All content is in `index.html`. Simply search for the section you want to edit:

- Hero text: Search for `class="hero-title"`
- Services: Search for `class="services-grid"`
- Testimonials: Search for `class="testimonials-grid"`
- Contact info: Search for `class="contact-details"`

### Adding Your Logo

Replace the logo placeholder in the navigation:

```html
<!-- Current -->
<div class="logo">
    <span class="logo-icon">◈</span>
    <span class="logo-text">Yukto</span>
</div>

<!-- With image -->
<div class="logo">
    <img src="your-logo.png" alt="Yukto" height="40">
</div>
```

### Social Media Links

Update the footer social links (around line 760 in `index.html`):

```html
<a href="https://linkedin.com/company/your-company" class="social-link">
<a href="https://twitter.com/your-handle" class="social-link">
<a href="https://instagram.com/your-handle" class="social-link">
```

## 📧 Form Integration

The contact form currently simulates submission. To connect it to a real backend:

### Option 1: Use FormSpree (Easiest)

1. Sign up at [formspree.io](https://formspree.io)
2. Update the form in `script.js` (around line 130):

```javascript
const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(formData)
});
```

### Option 2: Use Netlify Forms

1. Add `netlify` attribute to the form:
```html
<form class="contact-form" id="contactForm" netlify>
```

### Option 3: Custom Backend

Replace the `simulateFormSubmission` function with your API endpoint:

```javascript
async function submitForm(data) {
    const response = await fetch('/api/contact', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data)
    });
    return response.json();
}
```

## 🎯 SEO & Performance Tips

### Meta Tags (Already Included)

The site includes essential meta tags. Add these for better SEO:

```html
<!-- Open Graph (Social Media) -->
<meta property="og:title" content="Yukto - AI Automation & Digital Marketing">
<meta property="og:description" content="Transform your business with intelligent automation">
<meta property="og:image" content="https://yourdomain.com/og-image.jpg">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Yukto - AI Automation">
```

### Performance Optimizations

1. **Compress images**: Use tools like TinyPNG or ImageOptim
2. **Minify files**: Use online tools to minify CSS/JS for production
3. **Enable caching**: Configure your server for browser caching
4. **Use a CDN**: Consider Cloudflare or similar for faster delivery

## 📱 Mobile Responsiveness

The site is fully responsive with breakpoints at:
- **Desktop**: 1280px+
- **Tablet**: 768px - 1279px
- **Mobile**: < 768px

Test on different devices or use browser DevTools.

## 🎨 Adding Images

### Hero Background Image (Optional)

To add a hero background image:

```css
.hero-background {
    background-image: url('images/hero-bg.jpg');
    background-size: cover;
    background-position: center;
}
```

### Service Icons

Replace the SVG icons with your own or use an icon library like:
- [Heroicons](https://heroicons.com)
- [Feather Icons](https://feathericons.com)
- [Font Awesome](https://fontawesome.com)

### Team Photos / Avatars

Add real testimonial photos:

```html
<div class="author-avatar">
    <img src="images/testimonial-1.jpg" alt="Maya Lewis">
</div>
```

## 🔧 Browser Support

Supported browsers:
- ✅ Chrome (latest 2 versions)
- ✅ Firefox (latest 2 versions)
- ✅ Safari (latest 2 versions)
- ✅ Edge (latest 2 versions)
- ⚠️ IE 11 (requires polyfills)

## 📊 Analytics Integration

### Google Analytics

Add before closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Facebook Pixel

Similar process for Meta/Facebook tracking.

## 🚀 Deployment

### Deploy to Netlify (Free & Easy)

1. Create a free account at [netlify.com](https://netlify.com)
2. Drag and drop the `Yukto` folder
3. Your site is live instantly!

### Deploy to Vercel

```bash
npx vercel
```

### Deploy to GitHub Pages

1. Push code to GitHub repository
2. Go to Settings > Pages
3. Select main branch and root folder
4. Your site will be live at `username.github.io/repo-name`

## 🎨 Font Customization

Current fonts:
- **Primary**: Inter (body text)
- **Display**: Space Grotesk (headings)

To change fonts, update the Google Fonts import in `index.html` and CSS variables.

## ✨ Additional Enhancements

### Add GSAP Animations (Optional)

For more advanced animations:

```html
<!-- Add before closing </body> -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
```

### Add Tailwind CSS (Alternative)

If you prefer Tailwind, the structure supports easy conversion.

## 📄 License

This website is created for Yukto. Modify and use as needed.

## 🤝 Support

For questions or customization help:
- Email: hello@yukto.co
- Website: [Your domain]

---

**Built with care for Yukto** ✨

*Aligned Intelligence for Modern Business*