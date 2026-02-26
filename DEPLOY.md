# Deployment Guide

## Quick Deploy to GitHub Pages

### 1. Create a GitHub Repository

```bash
# In the sfp-website directory
git init
git add .
git commit -m "Initial commit: South Florida Psalter website"
```

### 2. Push to GitHub

```bash
# Create a new repository on GitHub first, then:
git remote add origin https://github.com/[username]/south-florida-psalter.git
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **main** branch
4. Click **Save**
5. Your site will be live at: `https://[username].github.io/south-florida-psalter/`

## Alternative Hosting Options

### Netlify (Drag & Drop)

1. Go to [netlify.com](https://netlify.com)
2. Sign up/login
3. Drag the `sfp-website` folder onto Netlify
4. Done! Instant deploy with custom domain option

### Vercel

```bash
npm i -g vercel
cd sfp-website
vercel
```

### Traditional Web Host

Upload all `.html` files to your web host via FTP. That's it!

## Custom Domain (Optional)

Once deployed, you can add a custom domain:

### GitHub Pages
- Add a `CNAME` file with your domain
- Configure DNS records to point to GitHub Pages

### Netlify/Vercel
- Go to Domain Settings
- Add custom domain
- Follow DNS instructions

## Testing Locally

Just open any `.html` file in your browser. No build process needed!

## Updates

To update the site:

1. Edit the HTML files
2. Commit changes: `git commit -am "Update content"`
3. Push to GitHub: `git push`
4. GitHub Pages automatically rebuilds

---

**Need help?** The site is 100% static HTML/CSS/JS. Any web host or static site service will work perfectly.
