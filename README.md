# SmartKids Tuition Portal

A modern, transparent tuition application and management system for Grace Community Church.

## Features

### Parent View
- Real-time application status tracking
- Clear timeline of application progress
- One-click payment (no QR maze!)
- Direct contact with visitation leaders

### Visitation Leader Dashboard
- Overview of all students in their zone
- Filterable student list by status
- Quick access to student info and parent contacts
- Action buttons for common tasks

## Demo

Toggle between "Parent View" and "Visitation Leader" using the switcher in the header.

## Deployment Options

### Option 1: Vercel (Recommended - Easiest)

1. **Via Vercel CLI:**
   ```bash
   npm install -g vercel
   cd church-tuition-portal
   vercel
   ```
   Follow the prompts - it will deploy in seconds!

2. **Via Vercel Dashboard:**
   - Go to https://vercel.com
   - Sign up/login with GitHub
   - Click "New Project"
   - Upload this folder or connect your GitHub repo
   - Deploy!

### Option 2: Netlify

1. **Via Netlify CLI:**
   ```bash
   npm install -g netlify-cli
   cd church-tuition-portal
   netlify deploy
   ```

2. **Via Netlify Dashboard:**
   - Go to https://netlify.com
   - Drag and drop this folder
   - Done!

### Option 3: GitHub Pages

1. Create a new GitHub repository
2. Upload these files
3. Go to Settings → Pages
4. Select "main" branch and "/" root
5. Your site will be live at `https://yourusername.github.io/repo-name`

### Option 4: Surge.sh (Super Quick)

```bash
npm install -g surge
cd church-tuition-portal
surge
```

### Option 5: Self-Hosting

Simply upload the files to any web server. The app is a single HTML file with no dependencies!

## Local Development

To run locally:

```bash
# Python 3
python3 -m http.server 8000

# OR Node.js
npx http-server

# Then open: http://localhost:8000
```

## Making it Production-Ready

This is currently a **demo/prototype**. To make it production-ready, you'll need:

1. **Backend Database**
   - Firebase/Supabase for real-time data
   - User authentication (separate parent/leader logins)

2. **Payment Integration**
   - Stripe for credit cards
   - PayNow for Singapore bank transfers

3. **Notifications**
   - Email (SendGrid/AWS SES)
   - SMS (Twilio)

4. **Admin Panel**
   - For church staff to approve applications
   - Manage fee waivers
   - Assign students to visitation leaders

## Tech Stack

- **Frontend**: Pure HTML/CSS/JavaScript (no frameworks needed for demo)
- **Fonts**: Google Fonts (Crimson Pro + DM Sans)
- **Responsive**: Mobile-first design

## License

MIT - Feel free to use and modify for your church needs!
