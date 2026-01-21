# 🚀 Quick Deployment Guide

## Fastest Method: Vercel (2 minutes)

### Method 1: Vercel CLI (Terminal)

```bash
# 1. Install Vercel CLI globally
npm install -g vercel

# 2. Navigate to the project folder
cd church-tuition-portal

# 3. Deploy!
vercel

# Follow the prompts:
# - Set up and deploy? Y
# - Which scope? (choose your account)
# - Link to existing project? N
# - What's your project's name? church-tuition-portal
# - In which directory is your code located? ./
# - Want to override the settings? N

# Done! You'll get a live URL like: https://church-tuition-portal.vercel.app
```

### Method 2: Vercel Website (No Code)

1. Go to https://vercel.com
2. Sign up with GitHub, GitLab, or Bitbucket
3. Click **"Add New..." → "Project"**
4. Click **"Browse"** or drag-and-drop the `church-tuition-portal` folder
5. Click **"Deploy"**
6. Wait 30 seconds... Done! 🎉

Your site will be live at: `https://church-tuition-portal-[random].vercel.app`

---

## Alternative: Netlify Drop (30 seconds)

1. Go to https://app.netlify.com/drop
2. Drag the `church-tuition-portal` folder onto the page
3. Done! You'll get a live URL instantly

---

## Alternative: Surge.sh (Terminal, 1 minute)

```bash
# 1. Install surge
npm install -g surge

# 2. Navigate and deploy
cd church-tuition-portal
surge

# Follow prompts:
# - Email: (your email)
# - Password: (create one)
# - Domain: church-tuition-portal.surge.sh (or custom)

# Done! Live at: http://church-tuition-portal.surge.sh
```

---

## Alternative: GitHub Pages (Free Forever)

### Via GitHub Desktop (Easiest)

1. Download GitHub Desktop: https://desktop.github.com
2. Create new repository: "church-tuition-portal"
3. Drag the project folder into GitHub Desktop
4. Commit and publish
5. Go to your repo on GitHub.com
6. Click **Settings → Pages**
7. Source: **Deploy from branch** → **main** → **/ (root)**
8. Save
9. Wait 2 minutes
10. Live at: `https://yourusername.github.io/church-tuition-portal`

### Via GitHub CLI

```bash
# 1. Install GitHub CLI
# macOS: brew install gh
# Windows: winget install GitHub.cli

# 2. Login
gh auth login

# 3. Create repo and push
cd church-tuition-portal
git init
git add .
git commit -m "Initial commit"
gh repo create church-tuition-portal --public --source=. --push

# 4. Enable GitHub Pages
gh repo edit --enable-pages --pages-branch main
```

---

## Don't Have Terminal Access?

### Use Vercel/Netlify Web Interface:

**Vercel:**
1. Zip the `church-tuition-portal` folder
2. Go to https://vercel.com/new
3. Upload the zip file
4. Deploy!

**Netlify:**
1. Go to https://app.netlify.com
2. Drag the `church-tuition-portal` folder
3. Drop!

---

## Troubleshooting

**Q: "vercel: command not found"**
- Make sure Node.js is installed: https://nodejs.org
- Try: `npm install -g vercel` again

**Q: "Permission denied"**
- Try: `sudo npm install -g vercel` (macOS/Linux)
- Or use Vercel website method instead

**Q: Page shows blank**
- Check browser console (F12)
- Make sure `index.html` is in the root folder

**Q: Want a custom domain?**
- Vercel: Project Settings → Domains → Add
- Netlify: Site Settings → Domain Management → Add custom domain

---

## What You'll Get

✅ Live, working demo app  
✅ HTTPS (automatic)  
✅ Fast global CDN  
✅ Free hosting (unless you need pro features)  
✅ Automatic deployments on updates  
✅ Custom domain support  

## Next Steps After Deployment

1. Share the URL with church leadership for feedback
2. Test on mobile devices
3. Gather requirements for backend (authentication, payments, database)
4. Consider booking a call to discuss the production build!

---

Need help? Feel free to ask! 🙌
