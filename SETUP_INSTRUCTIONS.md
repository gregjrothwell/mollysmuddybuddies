# V4 Setup Instructions

## Changes Made

✅ **Netlify Forms Integration** - Replaced Web3Forms with Netlify's built-in form handling
✅ **Image Swap** - Swapped collie image with rottweiler image in About section
✅ **Copy Updates** - Changed all copy from third person to first person (I/me)
✅ **Map Update** - Centered map on OL13 postcode
✅ **Instagram Feed** - Set up Instagram feed widget (requires configuration)

---

## 🔧 Netlify Forms Configuration

### What You Need to Do in Netlify:

1. **Deploy your site to Netlify** (via Git push or manual deploy)
2. **No additional setup needed!** Netlify Forms work automatically when deployed
3. **Access form submissions:**
   - Go to your Netlify dashboard
   - Click on your site
   - Navigate to **Forms** tab
   - All form submissions will appear here

### Form Features:
- ✅ Spam protection (honeypot field)
- ✅ AJAX submission (no page reload)
- ✅ Success/error messages
- ✅ All styling preserved

### Email Notifications (Optional):
To receive email notifications for new form submissions:
1. Go to **Site Settings** > **Forms** > **Form notifications**
2. Click **Add notification** > **Email notification**
3. Enter your email address
4. Save

### Netlify Forms Limits (Free Plan):
- 100 form submissions per month
- Unlimited forms
- Spam filtering included

---

## 📸 Instagram Feed Setup

The Instagram feed is set up using **Curator.io** (free tier available).

### Steps to Complete:

1. **Create a Curator.io Account:**
   - Go to [https://curator.io](https://curator.io)
   - Sign up for a free account

2. **Connect Your Instagram:**
   - In Curator dashboard, click **Add Source**
   - Select **Instagram**
   - Connect your @mollysmuddybuddies account

3. **Create a Feed:**
   - Click **Create Feed**
   - Choose **Grid** layout
   - Customize colors to match your site (optional)

4. **Get Your Embed Code:**
   - Click **Publish**
   - Copy your **Feed ID** (looks like: `abc123xyz`)

5. **Update index.html:**
   - Find line 629 in `index.html`
   - Replace `YOUR_CURATOR_ID` with your actual Feed ID:
   ```javascript
   i.src="https://cdn.curator.io/published/YOUR_CURATOR_ID.js";
   ```

### Alternative: Keep the Placeholder
If you prefer, you can keep the current Instagram placeholder (3 tiles linking to your Instagram). It looks clean and professional without requiring external services.

---

## 🚀 Deploying to Netlify

### Git-Based Deployment (Recommended):

You mentioned you already have Git initialized. Here's how to deploy:

1. **Check your Git remote:**
   ```bash
   cd v4
   git remote -v
   ```

2. **If no remote exists, create one:**
   - Create a new repository on GitHub/GitLab
   - Connect it:
   ```bash
   git remote add origin YOUR_REPO_URL
   ```

3. **Add and commit your changes:**
   ```bash
   git add .
   git commit -m "Initial v4 commit with Netlify Forms and updates"
   git push -u origin main
   ```

4. **Connect to Netlify:**
   - Log into [Netlify](https://netlify.com)
   - Click **Add new site** > **Import an existing project**
   - Connect your Git repository
   - Set **Base directory** to `v4` (if this is in a subdirectory)
   - Set **Publish directory** to `/` (root)
   - Click **Deploy site**

5. **Automatic Deployments:**
   - Every time you push to your repository, Netlify will automatically rebuild and deploy your site!

### Custom Domain (Optional):
1. In Netlify dashboard, go to **Domain settings**
2. Add your custom domain
3. Follow DNS configuration instructions

---

## 📍 Map Configuration

The map is now centered on postcode **OL13** at coordinates:
- Latitude: 53.7252525
- Longitude: -2.1970048

The location names (Weir, Bacup) remain as you requested.

---

## ✅ What's Working Now

1. **Contact Form** - Will work once deployed to Netlify
2. **Image Swap** - Complete (rottweiler now in About section)
3. **First Person Copy** - All "we/our" changed to "I/my"
4. **Map** - Centered on OL13
5. **Instagram Feed** - Ready (just needs Curator.io ID)

---

## 🆘 Need Help?

If you have questions about any of these setups, let me know and I can help troubleshoot!
