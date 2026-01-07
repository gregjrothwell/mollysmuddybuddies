# Deploy to Netlify - Complete Guide

## Why Netlify over GitHub Pages?

### Netlify Advantages ✅
- **Automatic deployments** - Push to GitHub → Auto-deploy
- **Better performance** - Global CDN (Content Delivery Network)
- **HTTPS for free** - Automatic SSL certificates
- **Custom domains easy** - Simple DNS setup
- **Serverless functions** - For future backend features (FREE)
- **Form handling** - Built-in form support (alternative to Web3Forms)
- **Deploy previews** - Test changes before going live
- **Instant rollbacks** - Undo deployments with one click
- **Better analytics** - Traffic and performance insights

### GitHub Pages Limitations ❌
- Manual updates required
- No serverless functions
- Slower global delivery
- Limited build options
- No deploy previews

**Verdict:** Netlify is MUCH better for your needs, especially for future booking systems!

---

## Part 1: Prepare Your Repository (5 minutes)

### Option A: Using Existing GitHub Repo
If you already have a GitHub repo:

1. **Navigate to v3 folder:**
   ```bash
   cd "/Users/gregrothwell/Documents/Mollys Muddy Buddies/v3"
   ```

2. **Check if it's a git repo:**
   ```bash
   git status
   ```

3. **If NOT a repo, initialize:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Molly's Muddy Buddies v3"
   ```

4. **Connect to GitHub:**
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/mollys-muddy-buddies.git
   git branch -M main
   git push -u origin main
   ```

### Option B: Create New Repo
If you don't have a repo:

1. Go to: https://github.com/new
2. Repository name: `mollys-muddy-buddies`
3. Description: `Dog walking service website for Molly's Muddy Buddies`
4. Public or Private (your choice - both work with Netlify)
5. Don't initialize with README (you'll push existing code)
6. Click "Create repository"

7. **Then follow these commands:**
   ```bash
   cd "/Users/gregrothwell/Documents/Mollys Muddy Buddies/v3"
   git init
   git add .
   git commit -m "Initial commit - Molly's Muddy Buddies v3"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/mollys-muddy-buddies.git
   git push -u origin main
   ```

---

## Part 2: Deploy to Netlify (3 minutes)

### Step 1: Sign Up for Netlify

1. Go to: https://app.netlify.com/signup
2. Click "Sign up with GitHub" (RECOMMENDED - easiest integration)
3. Authorize Netlify to access your GitHub account

### Step 2: Import Your Repository

1. Click "Add new site" → "Import an existing project"
2. Choose "Deploy with GitHub"
3. Authorize Netlify (if prompted)
4. Select your repository: `mollys-muddy-buddies`

### Step 3: Configure Build Settings

**You'll see a form - use these settings:**

- **Branch to deploy:** `main`
- **Build command:** (leave empty - it's a static site)
- **Publish directory:** `.` (just a dot)

Click "Deploy site"

### Step 4: Wait for Deployment (30 seconds)

Netlify will:
1. Pull your code from GitHub
2. Build the site
3. Deploy to their CDN
4. Give you a URL like: `https://random-name-12345.netlify.app`

---

## Part 3: Configure Custom Domain (Optional - 5 minutes)

### If You Have mollysmuddybuddies.com:

1. **In Netlify dashboard:**
   - Go to "Site settings" → "Domain management"
   - Click "Add custom domain"
   - Enter: `mollysmuddybuddies.com`
   - Click "Verify"

2. **Update DNS at your domain registrar:**

   **Option A - Netlify DNS (Easiest):**
   - Netlify will show you nameservers
   - Go to your domain registrar (GoDaddy, Namecheap, etc.)
   - Replace nameservers with Netlify's
   - Wait 24-48 hours for propagation

   **Option B - Keep Current DNS:**
   - Add A record: `75.2.60.5`
   - Add CNAME for www: `random-name-12345.netlify.app`

3. **Enable HTTPS:**
   - Netlify auto-provisions SSL certificate
   - Usually ready in 30 seconds
   - Your site will be https://mollysmuddybuddies.com

---

## Part 4: Set Up Auto-Deployment

**Already done!** When you connected GitHub, Netlify automatically set up:

✅ Push to `main` branch → Auto-deploy
✅ Pull requests → Deploy previews
✅ Rollback available in Netlify dashboard

### To Update Your Site:

```bash
# Make changes to your files
# Then:
git add .
git commit -m "Updated contact form"
git push
```

Netlify automatically deploys in ~30 seconds!

---

## Part 5: Netlify Configuration File (Optional but Recommended)

Create this file for better control:

**File: `/v3/netlify.toml`**

```toml
[build]
  publish = "."

[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
    Referrer-Policy = "strict-origin-when-cross-origin"

[[headers]]
  for = "*.js"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"

[[headers]]
  for = "*.css"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"

[[headers]]
  for = "*.jpg"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"

[[headers]]
  for = "*.png"
  [headers.values]
    Cache-Control = "public, max-age=31536000, immutable"
```

This adds:
- Security headers
- Better caching
- Handles single-page navigation

---

## Part 6: Alternative - Netlify Form Handling (Instead of Web3Forms)

Netlify has built-in form handling! Here's how to use it:

**Update your form in index.html:**

```html
<form name="contact" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
  <input type="hidden" name="form-name" value="contact">

  <!-- Hidden honeypot field -->
  <p style="display:none;">
    <label>Don't fill this out: <input name="bot-field"></label>
  </p>

  <div class="form-group">
    <label for="name">Your Name</label>
    <input type="text" id="name" name="name" required>
  </div>
  <!-- rest of your form fields -->
</form>
```

**Then in Netlify:**
- Go to "Forms" in dashboard
- Set up email notifications
- FREE for 100 submissions/month

---

## Quick Command Reference

### Initial Setup:
```bash
cd "/Users/gregrothwell/Documents/Mollys Muddy Buddies/v3"
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/mollys-muddy-buddies.git
git push -u origin main
```

### Future Updates:
```bash
git add .
git commit -m "Description of changes"
git push
```

### View Deployment:
- Go to: https://app.netlify.com
- See live site and deploy logs

---

## Troubleshooting

**Site not deploying?**
- Check Netlify deploy logs
- Verify publish directory is `.`
- Check all files are committed to git

**Images not loading?**
- Check file paths are relative (`images/logo.svg` not `/images/logo.svg`)
- Verify images are in git repo

**Custom domain not working?**
- DNS can take 24-48 hours
- Check nameservers are correct
- Use Netlify DNS for easiest setup

**Form not working?**
- Check Web3Forms access key is added
- Or switch to Netlify forms (see Part 6)

---

## Next Steps After Deployment

1. ✅ Test the live site
2. ✅ Test form submission
3. ✅ Check mobile responsiveness
4. ✅ Run Lighthouse audit
5. ✅ Set up custom domain
6. ✅ Add Google Analytics (optional)

---

## Support & Resources

- **Netlify Docs:** https://docs.netlify.com
- **Netlify Community:** https://answers.netlify.com
- **Deploy Status:** https://www.netlifystatus.com

---

## Cost

**100% FREE for your needs:**
- 100 GB bandwidth/month
- 300 build minutes/month
- Unlimited sites
- Free SSL
- Free CDN

This is MORE than enough for Molly's site!
