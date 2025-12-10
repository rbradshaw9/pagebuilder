# Live On Purpose - Funnel Pages

Professional landing pages and funnels for Live On Purpose webinars and offers.

## 🌐 Deployment

This project is deployed on Vercel at `go.drpauljenkins.com`

## 📁 Structure

```
/
├── index.html              # Root redirect to main site
├── vercel.json            # Vercel configuration
├── create-with-confidence/ # Individual funnel folder
│   ├── index.html         # Registration page
│   ├── confirmation.html  # Thank you page
│   └── assets/
│       └── css/
│           ├── styles.css
│           └── confirmation.css
└── [future-funnel]/       # Add new funnels here
```

## 🚀 Adding a New Funnel

1. **Copy the template folder:**
   ```bash
   cp -r create-with-confidence new-funnel-name
   ```

2. **Update the content:**
   - Edit `index.html` with your webinar/offer details
   - Edit `confirmation.html` with thank you page content
   - Update form action URLs for Infusionsoft/Keap
   - Customize colors in CSS files if needed

3. **Deploy:**
   ```bash
   git add .
   git commit -m "Add new funnel: [name]"
   git push
   ```
   Vercel will automatically deploy your changes.

## 🎨 Customization

### Colors
The default brand gradient is purple (`#667eea` to `#764ba2`). To customize:
- Edit `assets/css/styles.css` - search for gradient values
- Common locations: `.hero`, `.btn-primary`, `.bonus-section`

### Forms
Update the Infusionsoft form action URL:
```html
<form action="https://bl843.infusionsoft.com/app/form/process/YOUR_FORM_ID">
```

### Images
Add images to `assets/images/` folder within each funnel and reference them:
```html
<img src="assets/images/your-image.jpg" alt="Description">
```

## 📧 Integration

- **Infusionsoft/Keap**: Update form action URLs
- **Calendar Links**: Auto-generated for Google Calendar and Outlook
- **Social Sharing**: Update URLs in confirmation page

## 🔗 Live URLs

- **Root**: `go.drpauljenkins.com` → redirects to main site
- **Create with Confidence**: `go.drpauljenkins.com/create-with-confidence`

## 💡 Tips

- Test forms before going live
- Update social share URLs after deployment
- Keep CSS organized and reusable
- Use semantic HTML for better SEO
- Mobile-first responsive design included