# Portfolio Setup Instructions

## GitHub Pages Configuration

To deploy this portfolio website with your Namecheap domain:

### 1. Enable GitHub Pages

1. Go to your repository settings: `https://github.com/ZararSW/ZararSW/settings/pages`
2. Under "Build and deployment" → "Source", select **"GitHub Actions"**
3. The deployment workflow is already configured in `.github/workflows/deploy.yml`
4. Click "Save"

### 2. Configure Your Namecheap Domain

#### In Namecheap Dashboard:

1. Log in to your Namecheap account
2. Go to "Domain List" and click "Manage" next to your domain
3. Go to "Advanced DNS" tab
4. Add the following DNS records:

**A Records** (for apex domain):
```
Type: A Record
Host: @
Value: 185.199.108.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.109.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.110.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.111.153
TTL: Automatic
```

**CNAME Record** (for www subdomain):
```
Type: CNAME Record
Host: www
Value: zararsw.github.io
TTL: Automatic
```

### 3. Configure Custom Domain in GitHub Pages

1. In GitHub repository settings, go to "Pages"
2. Under "Custom domain", enter: `zararkolachi.me`
3. Click "Save"
4. Wait for DNS check to complete
5. Check "Enforce HTTPS" once DNS is verified

### 4. Update CNAME File (Already Done)

1. The `CNAME` file in this repository already contains: `zararkolachi.me`
2. No changes needed - the domain is preconfigured

### 5. Verify Setup

1. Wait 10-30 minutes for DNS propagation
2. Visit your domain to see if the portfolio is live
3. In GitHub repository settings under Pages, you should see "Your site is published at https://zararkolachi.me"

### 6. Enable HTTPS (Recommended)

1. In GitHub Pages settings, check "Enforce HTTPS"
2. This may take a few minutes to activate

### 7. Troubleshooting - Site Not Updating

If your site updates are not appearing:

1. **Clear browser cache**: Press `Ctrl+Shift+Delete` (or `Cmd+Shift+Delete` on Mac) and clear cached files
2. **Hard refresh**: Press `Ctrl+F5` (or `Cmd+Shift+R` on Mac) on your website
3. **Try incognito/private mode**: Open your site in a new incognito window
4. **Wait for deployment**: Check GitHub Actions tab to ensure the deployment workflow completed successfully
5. **Clear CDN cache**: If using Cloudflare or another CDN, purge the cache from their dashboard
6. **DNS propagation**: New domain changes may take up to 48 hours to fully propagate

The site includes cache-busting meta tags and versioned asset URLs to help prevent caching issues.

## Local Development

To test the portfolio locally:

```bash
# Navigate to the repository
cd /path/to/ZararSW

# Start a simple HTTP server
python3 -m http.server 8080

# Open browser and visit
# http://localhost:8080
```

## Customization

### Update Personal Information

Edit `index.html` to update:
- Email address
- LinkedIn profile URL
- GitHub username
- TryHackMe username (for badge)

### Modify Colors

Edit `style.css` and update CSS variables at the top:
```css
:root {
    --primary-color: #00ff88;
    --secondary-color: #00d4ff;
    --accent-color: #ff0055;
    /* ... */
}
```

### Add More Skills

Edit the skills section in `index.html` to add more technologies.

## Features

- ✨ Modern, cybersecurity-themed design
- 🎨 Smooth animations and transitions
- 📱 Fully responsive layout
- ⌨️ Typing animation effect
- 🖥️ Terminal-style code display
- 🎯 Smooth scrolling navigation
- 🌐 Integration with GitHub stats and TryHackMe
- 🎮 Easter egg (try the Konami code!)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

Feel free to use this template for your own portfolio. Just update the personal information!
