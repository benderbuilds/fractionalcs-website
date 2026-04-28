# FractionalCS Website

Professional landing page for fractional Customer Success leadership services — health tech focused, deployed at fractionalcs.io.

## Quick Deploy to Railway

### Prerequisites
- GitHub account (benderbuilds/fractionalcs-website)
- Railway account (https://railway.app)
- Domain: fractionalcs.io

### Push to GitHub

```bash
git add .
git commit -m "Update site"
git push
```

Railway auto-deploys on push (takes 1–2 minutes).

## Local Development

```bash
npm install
npm start
# Open http://localhost:3000
```

## File Structure

```
fractionalcs-website/
├── index.html          # Main website (single file)
├── jesse-bender.png    # Portrait photo used in Track Record section
├── package.json        # Node dependencies (serve)
├── railway.toml        # Railway config
├── .gitignore
└── README.md
```

## Customization

### Contact Form
The form uses Formspree (`https://formspree.io/f/xjggglaj`). Log in to Formspree to view submissions and manage notifications.

### Colors
Edit the CSS variables at the top of `index.html`:

```css
:root {
    --bg: #F7F4ED;          /* Warm off-white background */
    --bg-deep: #0F1B2A;     /* Dark navy (numbers section, footer, contact) */
    --ink: #0F1B2A;         /* Primary text */
    --accent: #E67E50;      /* Orange accent */
    --line: #E5DDD0;        /* Borders */
}
```

### Portrait
Replace `jesse-bender.png` in the project root. Displayed at 160×160px in the Track Record section.

### Updating Content
All content is in `index.html`. Key sections:
- **Hero** — headline and proof strip numbers
- **Numbers** — 6-metric grid
- **Use Cases** — 5 scenario cards
- **Track Record** — bio and role history
- **Ideal Client** — fit/no-fit lists
- **Contact** — Formspree form

## Deployment Notes

Site is deployed on Railway, connected to this GitHub repo. DNS is configured at your domain registrar pointing fractionalcs.io to Railway.

**To update the site:** commit changes and push — Railway deploys automatically.
