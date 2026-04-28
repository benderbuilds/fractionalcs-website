# FractionalCS.io - Quick Deployment Guide

## What I Built For You

✅ Professional, conversion-focused landing page
✅ Mobile-responsive design
✅ Clean, distinctive aesthetic (not generic AI look)
✅ All your content from the one-pager
✅ Ready to deploy to Railway
✅ Custom domain support (fractionalcs.io)

## 3-Step Deployment Process

### STEP 1: Create GitHub Repository (5 minutes)

1. Go to https://github.com/new
2. Repository name: `fractionalcs-website`
3. Keep it public
4. Click "Create repository"

Then in your terminal (in the fractionalcs-website folder):

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/fractionalcs-website.git
git branch -M main
git push -u origin main
```

### STEP 2: Deploy to Railway (3 minutes)

1. Go to https://railway.app and sign in
2. Click "+ New Project"
3. Select "Deploy from GitHub repo"
4. Choose `fractionalcs-website`
5. Railway auto-detects settings and deploys
6. Get your live URL (something like: https://fractionalcs-website.up.railway.app)
7. Test it!

### STEP 3: Connect Your Domain (10-60 minutes)

1. In Railway project → Settings → Domains
2. Click "+ Custom Domain"
3. Enter: `fractionalcs.io`
4. Railway gives you DNS records (CNAME or A record)
5. Go to your domain registrar (where you bought fractionalcs.io)
6. Add the DNS records Railway provides
7. Wait 10-60 mins for DNS to propagate
8. Done! Your site is live at https://fractionalcs.io

## Domain DNS Settings (You'll Need This)

When Railway gives you the DNS records, they'll look something like:

**Option A: CNAME Record**
- Type: CNAME
- Name: @ (or leave blank for root domain)
- Value: [Railway provides this, looks like: xyz.up.railway.app]

**Option B: A Record**
- Type: A
- Name: @
- Value: [Railway provides the IP address]

**For WWW subdomain:**
- Type: CNAME
- Name: www
- Value: fractionalcs.io (or the Railway URL)

## Testing Locally Before Deploying

If you want to preview the site on your computer first:

```bash
cd fractionalcs-website
npm install
npm start
```

Then open http://localhost:3000 in your browser.

## Quick Customizations

### Add Calendly Link
1. Open `index.html`
2. Find: `href="mailto:jesseinic@gmail.com"`
3. Replace with: `href="https://calendly.com/yourname/15min"`

### Change Phone/Email
Search in `index.html` for:
- `jesseinic@gmail.com`
- `319-430-5090`
- `linkedin.com/in/jesseinic`

Replace with your info.

### Change Colors
In `index.html`, find the CSS section at the top:

```css
:root {
    --primary: #1a3a52;    /* Change this for different blue */
    --accent: #e67e50;     /* Change this for different orange */
}
```

## Troubleshooting

**Site not showing after DNS update?**
- DNS can take up to 24 hours (usually 10-60 minutes)
- Clear your browser cache
- Try incognito/private browsing mode
- Check DNS propagation: https://dnschecker.org

**Railway deployment failed?**
- Check that all files are in the repository
- Make sure `package.json` exists
- Railway logs will show the error

**Need to update the site?**
1. Edit `index.html` locally
2. `git add . && git commit -m "Update content"`
3. `git push`
4. Railway auto-deploys the changes (takes 1-2 minutes)

## What's Included

- `index.html` - Your complete website (single file, easy to edit)
- `package.json` - Dependencies for hosting
- `railway.toml` - Railway configuration
- `.gitignore` - Keeps unnecessary files out of git
- `README.md` - Full documentation

## Next Steps After Launch

1. ✅ Test on mobile devices
2. ✅ Share URL with a few people for feedback
3. ✅ Set up Google Analytics (optional)
4. ✅ Add to your LinkedIn profile
5. ✅ Start your outreach campaign

## Need Help?

If you get stuck at any step, just let me know which step and what error you're seeing.

---

**Your site is ready to go live! 🚀**

The hardest part is over - you now have a professional site that positions you as an expert. Time to start reaching out to potential clients.
