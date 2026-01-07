# Formspree Setup Instructions

## Quick Setup (5 minutes)

1. **Go to https://formspree.io/**

2. **Sign Up**
   - Click "Get Started" or "Sign Up"
   - Use email: `mollysteele@hotmail.co.uk`
   - Create a password
   - Verify your email (check inbox)

3. **Create a New Form**
   - Click "+ New Form"
   - Form name: `Molly's Muddy Buddies Contact`
   - Email to receive submissions: `mollysteele@hotmail.co.uk`
   - Click "Create Form"

4. **Configure Email Subject**
   - In your form settings, look for "Email Notifications"
   - Set subject line to: `MUDDY BUDDY SUBMISSION`
   - (Note: This might be a paid feature - the free plan may use default subjects)

5. **Copy Your Form ID**
   - After creating the form, you'll see a form endpoint like:
     `https://formspree.io/f/xyzabc123`
   - Copy the part after `/f/` (e.g., `xyzabc123`)

6. **Update the Website**
   - Open `/v3/index.html`
   - Find line 310 (search for `your-form-id`)
   - Replace `your-form-id` with your actual form ID
   - Save the file

## What the Free Plan Includes
- ✅ 50 submissions per month
- ✅ Email notifications
- ✅ Spam filtering
- ✅ File uploads (up to 10MB)
- ✅ reCAPTCHA integration
- ❌ Custom subject lines (paid feature)
- ❌ Custom redirect after submission (paid feature)

## Alternative: Use Mailto Link

If you don't want to set up Formspree, you can use a simple mailto link instead.
This opens the user's email client directly.

Replace line 310 with:
```html
<form id="contactForm">
```

And add this JavaScript before the closing `</script>` tag:
```javascript
document.getElementById('contactForm').addEventListener('submit', function(e) {
  e.preventDefault();
  const name = document.getElementById('name').value;
  const email = document.getElementById('email').value;
  const phone = document.getElementById('phone').value;
  const message = document.getElementById('message').value;

  const subject = 'MUDDY BUDDY SUBMISSION';
  const body = `Name: ${name}%0D%0AEmail: ${email}%0D%0APhone: ${phone}%0D%0A%0D%0AMessage:%0D%0A${message}`;

  window.location.href = `mailto:mollysteele@hotmail.co.uk?subject=${subject}&body=${body}`;
});
```

Note: The mailto approach is less reliable as it depends on the user having an email client configured.
