# Web3Forms Setup (2 Minutes!)

## Why Web3Forms?
- ✅ **100% Free** - Unlimited submissions
- ✅ **No signup required** - Just get an API key
- ✅ **Spam protection** - Built-in reCAPTCHA
- ✅ **Email notifications** - Instant delivery
- ✅ **Custom subject lines** - FREE (unlike Formspree)
- ✅ **File uploads** - Support included

## Quick Setup

### Step 1: Get Your Access Key (30 seconds)

1. Go to: **https://web3forms.com/#get-started**
2. Enter email: `mollysteele@hotmail.co.uk`
3. Click "Get Access Key"
4. Check your email (mollysteele@hotmail.co.uk)
5. Click the verification link
6. Copy your access key (looks like: `abc123-def456-ghi789`)

### Step 2: Update index.html (Already Done!)

I've already updated your v3/index.html file with the Web3Forms code.

**All you need to do:**
1. Open `/v3/index.html`
2. Find line with: `value="YOUR_ACCESS_KEY_HERE"`
3. Replace `YOUR_ACCESS_KEY_HERE` with your actual access key
4. Save the file

**That's it!** The form will now send emails to mollysteele@hotmail.co.uk

## What the Form Will Send

**Subject:** Contact Form - Molly's Muddy Buddies
**To:** mollysteele@hotmail.co.uk

**Email will include:**
- Name
- Email address
- Phone number (if provided)
- Message about their dog

## Features You Get

### Built-in Spam Protection
- reCAPTCHA v3 (invisible, no checkboxes)
- Honeypot field (already added)
- Automatic spam filtering

### Success/Error Messages
- User sees success message after submission
- Redirects to thank you message
- Error handling included

### Email Format
Clean, professional emails with:
- All form data
- Sender's email for easy reply
- Timestamp
- User's IP (for security)

## Testing

After adding your access key:
1. Open index.html in browser
2. Fill out the form
3. Submit
4. Check mollysteele@hotmail.co.uk inbox
5. Should arrive within seconds!

## Advanced Options (Optional)

### Custom Subject Line
Already configured: "Contact Form - Molly's Muddy Buddies"

### Custom Redirect
After form submission, user stays on page with success message.
To redirect to a custom page, add:
```html
<input type="hidden" name="redirect" value="https://mollysmuddybuddies.com/thank-you">
```

### Auto-reply to Customer
Want to send an automatic confirmation email to the customer? Add:
```html
<input type="hidden" name="autoresponse" value="Thank you for contacting Molly's Muddy Buddies! We'll get back to you soon.">
```

## Troubleshooting

**Not receiving emails?**
1. Check spam folder
2. Verify access key is correct
3. Make sure email verification was completed
4. Check Web3Forms dashboard: https://web3forms.com/

**Form not submitting?**
1. Check browser console for errors
2. Verify access key is in the form
3. Make sure all required fields are filled

## Support

Web3Forms has great docs: https://docs.web3forms.com/

No account login needed - everything works with just your access key!
