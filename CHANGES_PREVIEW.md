# V4 Changes Preview - Ready for Your Review

## Summary of Changes Made

I've made three significant updates to the website. Please review these changes before we commit and deploy.

---

## 1. ✨ Font Update: Crimson Pro + Source Sans 3

**Changed from:** Cormorant Garamond (headings) + Nunito (body)
**Changed to:** Crimson Pro Bold (headings) + Source Sans 3 (body)

### Why This Works:
- **Crimson Pro** is a thick, strong serif font with excellent weight
- Slightly rustic feel that fits the outdoor/nature theme perfectly
- Much more substantial and bold than Cormorant Garamond
- **Source Sans 3** is a clean, readable sans-serif that pairs beautifully
- Still feminine enough but with much more presence and authority

### What's Updated:
- All headings (h1, h2, h3, h4)
- Logo text
- Footer text
- Button text uses Source Sans 3
- Blockquote uses Crimson Pro italic

**Visual Impact:** Headings now have significantly more weight and presence while maintaining elegance.

---

## 2. 🗺️ Custom Illustrated Map

**Replaced:** Google Maps embed with incorrect OL13 centering
**New:** Custom SVG illustrated map

### Features:
- **Stylized terrain** showing moorland and woodland areas
- **Markers for Bacup and Weir** with your brand colors (#c4a484 - rose)
- **Service radius circle** showing coverage area
- **Decorative paw prints** for character
- **Compass indicator** for orientation
- **"OL13 AREA" label** at the top
- **Matches your site aesthetic** - uses your exact color palette (moss, sage, bark, rose)

### Benefits:
- No more incorrect Google Maps centering issues
- Faster loading (no external iframe)
- Fully customizable - we control everything
- Unique and on-brand
- Shows exactly what you want to show

**Visual Style:** Organic, hand-drawn feel with soft edges and natural colors. Very fitting for a dog walking service in the countryside.

---

## 3. 💬 Floating WhatsApp Button

**Added:** Small WhatsApp bubble in bottom-right corner

### Behavior:
- **Appears after scrolling 400px** down the page (not visible on hero section)
- **Hides initially** to avoid cluttering the hero
- **Smooth fade-in/fade-out** animation
- **Hover effect:** Slightly scales up with enhanced shadow
- **Mobile optimized:** Smaller size on mobile (56px vs 60px)
- **Same WhatsApp link** as your main contact buttons

### UX Considerations:
- Only shows after user starts scrolling (non-intrusive)
- Fixed position so always accessible
- Doesn't block content (positioned in safe zone)
- Clean, minimal design - just the WhatsApp icon
- Industry-standard placement (bottom-right)

**Color:** WhatsApp green (#25D366) - instantly recognizable

---

## Files Modified

- `v4/index.html` - All changes applied
- `v4/CHANGES_PREVIEW.md` - This file (for your review)

---

## Next Steps - Awaiting Your Approval

Please review these changes and let me know:

1. **Font choice** - Do you like the thickness and style of Crimson Pro? Would you like to see alternatives?
2. **Map design** - Does the illustrated map style work for you? Any adjustments needed?
3. **WhatsApp button** - Is the behavior acceptable? Should it appear sooner/later?

### To Preview:
You can open `v4/index.html` in your browser to see all changes live.

### If Approved:
I'll:
1. Copy changes from v4 to v3 (Git repo)
2. Commit with descriptive message
3. Push to GitHub
4. Netlify will auto-deploy

### If Changes Needed:
Let me know what adjustments you'd like and I'll refine before deployment.

---

## Visual Comparison

### Fonts:
- **Before:** Thin, delicate Cormorant Garamond
- **After:** Bold, substantial Crimson Pro with strong weight

### Map:
- **Before:** Google Maps iframe (centering issues)
- **After:** Custom illustrated map with your brand colors and style

### Contact:
- **Before:** Only contact section buttons
- **After:** Plus floating WhatsApp button for easy access while scrolling

---

**Ready for your feedback!** 🐾
