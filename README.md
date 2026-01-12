# Skylark Software LLC - Company Website

Official company website for Skylark Software LLC, built for GitHub Pages.

## Overview

This website serves as the official web presence for Skylark Software LLC and provides required pages for App Store compliance:
- Privacy Policy (required for App Store submissions)
- Support page (recommended for App Store)
- Terms of Service
- Company information

## Live Site

Once deployed, the site will be available at:
- **Primary:** https://skylarksoftware.me
- **GitHub Pages:** https://skylark-software.github.io/[repo-name]/

## Pages Included

- `index.html` - Company landing page
- `privacy.html` - Privacy Policy (REQUIRED for App Store)
- `support.html` - Support and contact information
- `terms.html` - Terms of Service
- `css/style.css` - Responsive stylesheet

## Deployment to GitHub Pages

### Option 1: Create skylark-software.github.io Repository (Recommended)

1. **Create repository on GitHub:**
   ```bash
   # Go to github.com and create a new repository named:
   # skylark-software.github.io
   ```

2. **Initialize git and push:**
   ```bash
   cd ~/skylark-software/website
   git init
   git add .
   git commit -m "Initial commit: Skylark Software company website"
   git branch -M main
   git remote add origin git@github.com:skylark-software/skylark-software.github.io.git
   git push -u origin main
   ```

3. **Site will automatically be live at:**
   - https://skylark-software.github.io
   - https://skylarksoftware.me (after DNS configuration)

### Option 2: Use a Named Repository

1. **Create repository on GitHub:**
   ```bash
   # Create a repository with any name, e.g., "website" or "company-site"
   ```

2. **Push code:**
   ```bash
   cd ~/skylark-software/website
   git init
   git add .
   git commit -m "Initial commit: Skylark Software company website"
   git branch -M main
   git remote add origin git@github.com:skylark-software/website.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Navigate to "Pages" section
   - Under "Source", select "main" branch
   - Click "Save"

## Custom Domain Configuration (skylarksoftware.me)

### Step 1: Configure DNS at Your Domain Registrar

Add the following DNS records:

**For apex domain (skylarksoftware.me):**
```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**For www subdomain (optional):**
```
Type: CNAME
Name: www
Value: skylark-software.github.io
```

### Step 2: Configure Custom Domain in GitHub

1. Go to your repository Settings > Pages
2. Under "Custom domain", enter: `skylarksoftware.me`
3. Click "Save"
4. Wait for DNS check to complete (may take a few minutes)
5. Enable "Enforce HTTPS" once DNS is verified

### Step 3: Verify CNAME File

The `CNAME` file in this repository should contain:
```
skylarksoftware.me
```

This file tells GitHub Pages which custom domain to use.

## DNS Propagation

After configuring DNS:
- Changes can take 24-48 hours to fully propagate
- Use https://www.whatsmydns.net to check propagation status
- Test with: `dig skylarksoftware.me` or `nslookup skylarksoftware.me`

## Local Development

To preview the site locally:

1. **Using Python (simple HTTP server):**
   ```bash
   cd ~/skylark-software/website
   python3 -m http.server 8000
   # Visit http://localhost:8000 in your browser
   ```

2. **Using VS Code Live Server:**
   - Install "Live Server" extension
   - Right-click `index.html` and select "Open with Live Server"

## URLs for App Store Connect

Once deployed, use these URLs in App Store Connect:

- **Privacy Policy:** https://skylarksoftware.me/privacy.html
- **Support URL:** https://skylarksoftware.me/support.html
- **Marketing URL:** https://skylarksoftware.me

## Customization

### Update Email Addresses

Replace placeholder email addresses in these files:
- `privacy.html` - privacy@skylarksoftware.me
- `support.html` - support@skylarksoftware.me
- `terms.html` - legal@skylarksoftware.me

You'll need to set up these email addresses (or use a catch-all).

### Update Content

1. **Add app information:**
   - Edit `index.html` to add more apps as they're developed
   - Update the "Our Apps" section

2. **Customize privacy policy:**
   - Review `privacy.html` and update based on your specific app's data practices
   - Update the "Last Updated" date when making changes

3. **Add company details:**
   - Update the "About Us" section in `index.html`
   - Add team member information if desired

### Styling

All styles are in `css/style.css`:
- Modify CSS variables at the top to change colors/fonts
- Responsive breakpoints are at 768px and 480px
- Clean, modern design works well on all devices

## File Structure

```
website/
├── index.html          # Homepage
├── privacy.html        # Privacy Policy (required for App Store)
├── support.html        # Support page
├── terms.html          # Terms of Service
├── CNAME              # GitHub Pages custom domain config
├── README.md          # This file
├── .gitignore         # Git ignore rules
└── css/
    └── style.css      # All styles
```

## Maintenance

### Updating Content

1. Edit files locally
2. Test changes using local server
3. Commit and push:
   ```bash
   git add .
   git commit -m "Update: describe your changes"
   git push
   ```
4. Changes will be live within 1-2 minutes

### Regular Updates

- Review and update Privacy Policy annually or when data practices change
- Update Terms of Service as needed
- Keep contact information current
- Update copyright year annually

## Troubleshooting

### Site not loading after deployment
- Check GitHub Pages is enabled in repository settings
- Verify DNS records are correct
- Wait for DNS propagation (up to 48 hours)
- Check GitHub Pages build status

### HTTPS not working
- Wait for DNS verification to complete
- Enable "Enforce HTTPS" in GitHub Pages settings
- May take a few hours after domain verification

### Custom domain not working
- Verify CNAME file contains exactly: `skylarksoftware.me`
- Check DNS records at registrar
- Use `dig skylarksoftware.me` to verify DNS propagation

## Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Custom Domain Setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [App Store Connect](https://appstoreconnect.apple.com)

## License

Copyright 2026 Skylark Software LLC. All rights reserved.
