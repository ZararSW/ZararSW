# Portfolio Setup Instructions

## GitHub Pages Configuration

To deploy this portfolio website with your Namecheap domain:

### 1. Enable GitHub Pages

1. Go to your repository settings: `https://github.com/ZararSW/ZararSW/settings/pages`
2. Under "Source", select the branch you want to deploy (usually `main` or `master`)
3. Select the root folder `/` as the source
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

### 3. Update CNAME File

1. Update the `CNAME` file in this repository with your actual domain name
2. For example, if your domain is `zaraahmed.com`, the CNAME file should contain:
   ```
   zaraahmed.com
   ```

### 4. Verify Setup

1. Wait 10-30 minutes for DNS propagation
2. Visit your domain to see if the portfolio is live
3. In GitHub repository settings under Pages, you should see "Your site is published at https://yourdomain.com"

### 5. Enable HTTPS (Recommended)

1. In GitHub Pages settings, check "Enforce HTTPS"
2. This may take a few minutes to activate

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
