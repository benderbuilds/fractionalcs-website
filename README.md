# FractionalCS Website

Professional landing page for fractional Customer Success leadership services.

## Quick Deploy to Railway

### Prerequisites
- GitHub account
- Railway account (https://railway.app)
- Domain: fractionalcs.io

### Step 1: Push to GitHub

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - FractionalCS website"

# Create a new repository on GitHub (https://github.com/new)
# Name it: fractionalcs-website

# Add remote and push
git remote add origin https://github.com/YOUR_USERNAME/fractionalcs-website.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy to Railway

1. Go to https://railway.app
2. Click "New Project"
3. Select "Deploy from GitHub repo"
4. Connect your GitHub account if not already connected
5. Select the `fractionalcs-website` repository
6. Railway will automatically detect the configuration and deploy
7. Once deployed, you'll get a URL like `https://fractionalcs-website.up.railway.app`

### Step 3: Connect Custom Domain

1. In Railway dashboard, click on your project
2. Go to Settings → Domains
3. Click "Add Domain"
4. Enter: `fractionalcs.io`
5. Railway will provide DNS records (usually a CNAME)
6. Go to your domain registrar (where you bought fractionalcs.io)
7. Add the DNS records Railway provides:
   - Type: CNAME or A record (depending on what Railway gives you)
   - Name: @ (for root domain) or www
   - Value: [Railway provides this]
8. Wait 5-60 minutes for DNS propagation
9. Your site will be live at https://fractionalcs.io

### Alternative: Redirect www to root domain

If you want both www.fractionalcs.io and fractionalcs.io to work:
1. Add both domains in Railway
2. Set one as primary
3. Configure DNS at your registrar for both

## Local Development

To test locally:

```bash
# Install dependencies
npm install

# Start local server
npm start

# Open browser to http://localhost:3000
```

## File Structure

```
fractionalcs-website/
├── index.html          # Main website file
├── package.json        # Node dependencies
├── railway.toml        # Railway configuration
└── README.md          # This file
```

## Customization

### Update Contact Info
Edit `index.html` and find:
- Email: `jesseinic@gmail.com`
- LinkedIn: `linkedin.com/in/jesseinic`
- Phone: `319-430-5090`

### Add Calendly Link
If you want to add a Calendly scheduling link:
1. Find "Schedule 15-Min Call" buttons
2. Replace `mailto:jesseinic@gmail.com` with your Calendly link
3. Example: `https://calendly.com/yourname/15min`

### Change Colors
Edit the CSS variables in `index.html`:
```css
:root {
    --primary: #1a3a52;      /* Main blue color */
    --accent: #e67e50;       /* Orange accent */
    --text: #2c3e50;         /* Main text color */
    --text-light: #546e7a;   /* Secondary text */
    --bg: #fafbfc;           /* Background */
}
```

## Support

For questions about deployment, contact Jesse at jesseinic@gmail.com
