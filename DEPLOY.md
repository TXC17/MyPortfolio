# Deployment Guide

## ✅ Project Structure Organized

Your portfolio is now properly organized:
```
MyPortfolio/
├── assets/
│   ├── css/styles.css
│   ├── js/script.js
│   └── images/
├── index.html
└── deployment configs
```

## GitHub Pages Deployment

### ✅ Already Configured!
Your project is ready to deploy. The GitHub Actions workflow is already set up.

### Step 1: Enable GitHub Pages
1. Go to your repository: https://github.com/TXC17/MyPortfolio
2. Click on **Settings**
3. Scroll down to **Pages** section
4. Under "Build and deployment":
   - Source: Select **GitHub Actions**
5. Save the changes

### Step 2: Monitor Deployment
- Go to the **Actions** tab in your repository
- Watch the deployment workflow run
- Once complete (green checkmark), your site is live!

Your site will be available at: `https://txc17.github.io/MyPortfolio/`

---

## Custom Server Deployment

### Option 1: FTP/SFTP Upload
1. Connect to your server using an FTP client (FileZilla, WinSCP, etc.)
2. Upload these files to your web root directory (usually `public_html` or `www`):
   - `index.html`
   - `styles.css`
   - `script.js`
   - All image files
   - Any other assets

### Option 2: SSH/Command Line
```bash
# Connect to your server
ssh user@your-server.com

# Navigate to web root
cd /var/www/html

# Clone or upload your files
git clone https://github.com/TXC17/[your-repo].git .

# Or use rsync from local machine
rsync -avz --exclude '.git' ./ user@your-server.com:/var/www/html/
```

### Option 3: cPanel File Manager
1. Log into your cPanel
2. Open **File Manager**
3. Navigate to `public_html`
4. Upload all files
5. Extract if uploaded as zip

### Server Requirements
- Web server (Apache, Nginx, or any static file server)
- No special server-side requirements (pure HTML/CSS/JS)
- HTTPS recommended for security

### Testing
After deployment, visit your domain and verify:
- All pages load correctly
- Images display properly
- Navigation works
- Contact links function
- Responsive design on mobile

---

## Troubleshooting

### GitHub Pages not showing
- Check Actions tab for deployment errors
- Ensure Pages is enabled in Settings
- Wait 2-3 minutes for DNS propagation

### Custom server issues
- Verify file permissions (644 for files, 755 for directories)
- Check .htaccess if using Apache
- Ensure index.html is in the correct directory
- Clear browser cache

### Assets not loading
- Check file paths are relative, not absolute
- Verify all files were uploaded
- Check browser console for 404 errors
