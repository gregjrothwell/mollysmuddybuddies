# Molly's Muddy Buddies - v3

## 🚀 Quick Start

### 1. Set Up Web3Forms (2 minutes)
See **WEB3FORMS_SETUP.md** for instructions
- Get free access key from web3forms.com
- Replace `YOUR_ACCESS_KEY_HERE` in index.html (line 433)
- Form sends to: mollysteele@hotmail.co.uk

### 2. Deploy to Netlify (5 minutes)
See **NETLIFY_DEPLOYMENT.md** for complete guide
- Sign up at netlify.com with GitHub
- Connect your repo
- Auto-deploys on every push!

---

## What's New in v3

### ✅ Enhanced SEO & Meta Tags
- Complete Open Graph tags for Facebook sharing
- Twitter Card meta tags for Twitter sharing
- Comprehensive schema.org LocalBusiness structured data
- Additional SEO meta tags (keywords, robots, author, language, canonical URL)
- Favicon support with multiple sizes

### ✅ Updated Google Maps
- **Primary location: Weir** (coordinates: 53.7252525, -2.1970048)
- Map displays "Weir, Bacup, Rossendale" to cover both service areas
- Zoomed to show both locations
- Schema.org geo-coordinates set to Weir as primary location

### ✅ Logo & Branding
- Logo with green background (#6b8e5e - moss green)
- All required favicon files generated:
  - `favicon.svg` - SVG favicon
  - `favicon-32x32.png` - 32x32 PNG
  - `favicon-16x16.png` - 16x16 PNG
  - `apple-touch-icon.png` - 180x180 PNG for Apple devices
  - `og-image.jpg` - 1200x630 JPG for social media sharing

### ✅ Contact Form - Web3Forms Integration
- FREE unlimited submissions
- Custom subject line: "Contact Form - Molly's Muddy Buddies"
- Spam protection (honeypot + reCAPTCHA)
- Success/error messages
- Loading state with spinner
- Auto-clears form after submission

### ✅ Security Improvements
- Added `rel="noopener"` to all external links
- SRI hash on Font Awesome CDN
- Netlify security headers configured

### ✅ Performance
- Lazy loading on gallery images
- Optimized favicon files
- Netlify CDN caching configured

### ✅ Accessibility
- Autocomplete attributes on form fields
- ARIA labels on mobile menu
- Proper focus management

---

## Files Generated

All image assets are located in `/v3/images/`:
- logo.svg (87KB with embedded image + green background)
- favicon.svg (87KB)
- favicon-32x32.png (3.1KB)
- favicon-16x16.png (1.3KB)
- apple-touch-icon.png (51KB)
- og-image.jpg (117KB)

---

## Configuration Files

- **netlify.toml** - Netlify deployment configuration
  - Security headers
  - Cache control
  - Redirects

- **index.html** - Main website file
  - Line 433: Add Web3Forms access key here

---

## To-Do Before Launch

- [ ] Get Web3Forms access key (WEB3FORMS_SETUP.md)
- [ ] Add access key to index.html line 433
- [ ] Test form submission
- [ ] Deploy to Netlify (NETLIFY_DEPLOYMENT.md)
- [ ] Set up custom domain (if applicable)
- [ ] Test on mobile devices
- [ ] Run Lighthouse audit

---

## Service Areas

Primary: **Weir**
Secondary: **Bacup**

Both locations are properly represented in:
- Google Maps embed (zoomed to show both)
- Schema.org structured data
- Meta descriptions
- Page content

---

## Contact Information

- Email: mollysteele@hotmail.co.uk
- Phone: +447896015851
- Facebook: https://www.facebook.com/profile.php?id=100092157014465
- Instagram: @mollysmuddybuddies
- Messenger: m.me/100092157014465
- WhatsApp: wa.me/447896015851

---

## Documentation

- **WEB3FORMS_SETUP.md** - Form setup instructions
- **NETLIFY_DEPLOYMENT.md** - Complete deployment guide
- **IMPROVEMENTS_SUMMARY.md** - All fixes and recommendations
- **FORMSPREE_SETUP.md** - Alternative form service (if needed)

---

## Tech Stack

- HTML5
- CSS3 (inline, minified)
- Vanilla JavaScript
- Web3Forms API
- Google Fonts (Cormorant Garamond + Nunito)
- Font Awesome 6.4.0
- Netlify hosting

---

## Support

For questions about:
- **Web3Forms**: https://docs.web3forms.com
- **Netlify**: https://docs.netlify.com
- **This website**: Check the documentation files in this folder
