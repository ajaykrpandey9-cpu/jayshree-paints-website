# QUICK START TERMINAL COMMANDS

## 1️⃣ WINDOWS SETUP (PowerShell or Command Prompt)

### Using Python 3 (Recommended if Python is installed)
```powershell
# Navigate to project folder
cd "C:\Users\je264\OneDrive\Desktop\Desktop\Code\JE Website\jayshree-paints-website"

# Start local development server
python -m http.server 8000

# Open browser at: http://localhost:8000
# To stop server: Press Ctrl+C
```

### Using Python 2
```powershell
cd "C:\Users\je264\OneDrive\Desktop\Desktop\Code\JE Website\jayshree-paints-website"
python -m SimpleHTTPServer 8000
# Open: http://localhost:8000
```

### Using Node.js (http-server)
```powershell
# Install http-server (first time only)
npm install -g http-server

# Navigate to project
cd "C:\Users\je264\OneDrive\Desktop\Desktop\Code\JE Website\jayshree-paints-website"

# Start server
http-server -p 8000

# Open: http://localhost:8000
```

### Using PHP
```powershell
cd "C:\Users\je264\OneDrive\Desktop\Desktop\Code\JE Website\jayshree-paints-website"
php -S localhost:8000
# Open: http://localhost:8000
```

---

## 2️⃣ MAC / LINUX SETUP

### Using Python 3 (Built-in, Recommended)
```bash
cd ~/Desktop/Code/JE\ Website/jayshree-paints-website
python3 -m http.server 8000
# Open: http://localhost:8000
# Stop: Ctrl+C
```

### Using Python 2
```bash
cd ~/Desktop/Code/JE\ Website/jayshree-paints-website
python -m SimpleHTTPServer 8000
# Open: http://localhost:8000
```

### Using Node.js (http-server)
```bash
# Install (first time)
npm install -g http-server

# Start
cd ~/Desktop/Code/JE\ Website/jayshree-paints-website
http-server -p 8000
```

### Using PHP
```bash
cd ~/Desktop/Code/JE\ Website/jayshree-paints-website
php -S localhost:8000
# Open: http://localhost:8000
```

### Using Ruby (if installed)
```bash
cd ~/Desktop/Code/JE\ Website/jayshree-paints-website
ruby -run -ehttpd . -p8000
```

---

## 3️⃣ VS CODE - LIVE SERVER (Easiest!)

```
1. Install "Live Server" extension
   - Open VS Code
   - Extensions (Ctrl+Shift+X)
   - Search "Live Server"
   - Click Install

2. Launch
   - Right-click on index.html
   - Select "Open with Live Server"
   - Browser opens automatically
   - Any file change = auto-refresh!

3. Stop
   - Click "Go Live" button (bottom right) to toggle off
```

---

## 4️⃣ BUILD FOR PRODUCTION

### Create Production Folder
```powershell
# Windows
mkdir jayshree-paints-production
copy-item jayshree-paints-website\* jayshree-paints-production -Recurse

# Mac/Linux
mkdir jayshree-paints-production
cp -r jayshree-paints-website/* jayshree-paints-production/
```

### Minify CSS (Optional, using online tools)
```
Visit: https://cssminifier.com
Paste content from assets/styles/style.css
Download and replace
```

### Minify JavaScript (Optional)
```
Visit: https://jsminifier.com
Paste content from assets/js/script.js
Download and replace
```

---

## 5️⃣ DEPLOYMENT COMMANDS

### Deploy to Netlify (via Terminal)
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Navigate to project
cd jayshree-paints-website

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod

# Your site is live! 🎉
```

### Deploy to Vercel (via Terminal)
```bash
# Install Vercel CLI
npm install -g vercel

# Navigate to project
cd jayshree-paints-website

# Deploy
vercel --prod

# Your site is live! 🎉
```

### Deploy to GitHub Pages
```bash
# Initialize Git repo
git init

# Add all files
git add .

# First commit
git commit -m "Initial Jayshree Paints website"

# Add remote (replace with your GitHub repo URL)
git remote add origin https://github.com/yourusername/jayshree-paints-website.git

# Push to GitHub
git branch -M main
git push -u origin main

# Go to GitHub Settings > Pages > Select 'main' branch
# Your site is live! 🎉
```

---

## 6️⃣ COMMON UPDATES

### Update Shop Phone Number
```bash
# Find and replace 9953787727 with your number
# In all files:
- index.html (multiple places)
- assets/js/script.js
- schema-markup.html
```

### Update Shop Email
```bash
# Find and replace J264003@gmail.com with your email
# In all files:
- index.html (multiple places)
- schema-markup.html
```

### Update Address
```bash
# Edit HTML: Open index.html
# Find: "SH 15A, Main Road, Preetnagar..."
# Replace with your actual address (2 places)
```

### Update Operating Hours
```bash
# Edit HTML: Open index.html
# Find: <table class="hours-table">
# Update hours for each day (Monday-Sunday)
```

### Add New Product
```javascript
// In assets/js/script.js, find productsData array
// Add new object:
{
    id: 13,
    name: 'Product Name',
    category: 'paints', // or hardware, materials, tools
    description: 'Product description',
    price: '₹price',
    stock: 'In Stock',
    isNew: false,
    image: '🎨' // Change emoji or add image URL
}
```

### Add New Review
```javascript
// In assets/js/script.js, find reviewsData array
// Add new object:
{
    id: 7,
    author: 'Customer Name',
    rating: 5,
    text: 'Great products and service!',
    date: '1 week ago'
}
```

---

## 7️⃣ TESTING COMMANDS

### Check File Structure
```bash
# Windows (PowerShell)
tree jayshree-paints-website

# Mac/Linux
tree jayshree-paints-website
# or
ls -laR jayshree-paints-website
```

### Validate HTML
```bash
# Use online validators:
# https://validator.w3.org/
# Upload index.html and check for errors
```

### Test Responsiveness
```bash
# Open website in browser
# Press F12 (open DevTools)
# Click Ctrl+Shift+M (Toggle Device Toolbar)
# Test on different screen sizes:
# - Desktop (1200px+)
# - Tablet (768px)
# - Mobile (375px)
```

### Test Performance
```bash
# Use Lighthouse (built into Chrome DevTools)
1. Open website
2. Press F12
3. Go to "Lighthouse" tab
4. Click "Analyze page load"
5. View performance score (goal: 90+)
```

---

## 8️⃣ TROUBLESHOOTING COMMANDS

### Port Already in Use (8000 is occupied)
```bash
# Use different port
python -m http.server 8080
# Open: http://localhost:8080
```

### Clear Browser Cache
```
Windows: Ctrl+Shift+Delete
Mac: Command+Shift+Delete
# Or in browser settings > Clear browsing data
```

### Check for JavaScript Errors
```
1. Open website
2. Press F12 (DevTools)
3. Go to "Console" tab
4. Look for red error messages
5. Fix errors in assets/js/script.js
```

### Check CSS Issues
```
1. Open website
2. Press F12 (DevTools)
3. Go to "Elements" tab
4. Hover over elements
5. Check computed styles
6. Fix in assets/styles/style.css
```

---

## 9️⃣ ADVANCED: BUILD WORKFLOW

### Watch File Changes (Auto-reload)
```bash
# Install nodemon
npm install -g nodemon

# Watch and reload on changes
nodemon --exec "python -m http.server 8000" --watch . --ext html,css,js
```

### Version Control (Git)
```bash
# Initialize git repo
git init

# Configure git (first time)
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Add all files
git add .

# Create backup commit
git commit -m "v1.0 - Jayshree Paints Website Launch"

# View history
git log --oneline
```

### Backup Project
```bash
# Windows
robocopy jayshree-paints-website C:\backup\jayshree-paints-backup-v1 /E /V

# Mac/Linux
rsync -av jayshree-paints-website/ ~/backup/jayshree-paints-backup-v1/
```

---

## 🔟 VERIFICATION CHECKLIST

Run these commands to verify everything is working:

```bash
# 1. Check all HTML is valid
# Use: https://validator.w3.org/

# 2. Check all CSS is valid
# Use: https://jigsaw.w3.org/css-validator/

# 3. Check for broken links
# Use: https://www.brokenlinkcheck.com/

# 4. Check mobile responsive
# Use: https://responsivedesignchecker.com/

# 5. Check page speed
# Use: https://pagespeed.web.dev/

# 6. Check SEO
# Use: https://seositecheckup.com/

# 7. Test WhatsApp links
# Click each WhatsApp button and verify it opens
```

---

## 📊 DEVELOPER CONSOLE LOGGING

View messages in browser console:
```javascript
// You'll see:
✅ Jayshree Paints & Hardware Website - Fully Loaded
📱 Mobile Responsive: Yes
♿ Accessibility: WCAG AA Compliant
⚡ Performance Optimized: Yes
📊 Analytics Ready: Integrate with Google Analytics
```

This means website is working perfectly! ✨

---

## 🚀 DEPLOYMENT SUMMARY

| Method | Time | Cost | Difficulty |
|--------|------|------|-----------|
| Netlify | 5 min | Free | ⭐ Easy |
| Vercel | 5 min | Free | ⭐ Easy |
| GitHub Pages | 10 min | Free | ⭐⭐ Medium |
| Traditional Hosting | 30 min | ₹500-2000 | ⭐⭐ Medium |
| AWS/DigitalOcean | 1-2 hrs | ₹1000+ | ⭐⭐⭐ Hard |

**Recommendation for beginners:** Start with Netlify! ✨

---

## 💡 FINAL TIPS

1. **Always test locally first** before deploying
2. **Keep a backup** of your files
3. **Update content regularly** (products, reviews)
4. **Monitor analytics** weekly
5. **Respond to inquiries quickly** (within 1 hour)
6. **Collect customer feedback** for improvements
7. **Update social media links** after domain setup

---

**Happy Launching! 🎨 Make your shop shine online! 🚀**
