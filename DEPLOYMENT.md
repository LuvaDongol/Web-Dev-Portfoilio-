# Deployment Guide

This guide will help you deploy your portfolio website to various hosting platforms. Since this is a static website (HTML, CSS, JavaScript), it can be deployed for free on multiple platforms.

## Table of Contents
- [Option 1: GitHub Pages (Recommended)](#option-1-github-pages-recommended)
- [Option 2: Netlify](#option-2-netlify)
- [Option 3: Vercel](#option-3-vercel)
- [Option 4: Local Testing](#option-4-local-testing)

---

## Option 1: GitHub Pages (Recommended)

GitHub Pages is the easiest option since your code is already on GitHub.

### Steps:

1. **Push your code to GitHub** (already done)

2. **Enable GitHub Pages:**
   - Go to your repository: https://github.com/LuvaDongol/Web-Dev-Portfoilio-
   - Click on **Settings** tab
   - Scroll down to **Pages** section in the left sidebar
   - Under "Source", select **Deploy from a branch**
   - Select branch **main** (or **master**) and folder **/ (root)**
   - Click **Save**

3. **Wait for deployment:**
   - GitHub will automatically deploy your site
   - This usually takes 1-3 minutes
   - Your site will be available at: `https://luvalidongol.github.io/Web-Dev-Portfoilio-/`

4. **View your site:**
   - Once deployed, you'll see the URL in the Pages settings
   - Click the "Visit site" button or navigate to the URL

### Custom Domain (Optional)
If you want to use your own domain:
1. Add a `CNAME` file to your repository with your domain name
2. Configure your domain's DNS settings to point to GitHub Pages
3. Update the custom domain in GitHub Pages settings

---

## Option 2: Netlify

Netlify offers continuous deployment and is very beginner-friendly.

### Steps:

1. **Create a Netlify account:**
   - Go to https://www.netlify.com
   - Sign up with your GitHub account

2. **Deploy your site:**
   - Click **Add new site** → **Import an existing project**
   - Choose **GitHub** as your Git provider
   - Authorize Netlify to access your repositories
   - Select your `Web-Dev-Portfoilio-` repository

3. **Configure build settings:**
   - Base directory: Leave empty (or `.`)
   - Build command: Leave empty (no build needed)
   - Publish directory: Leave empty (or `.`)
   - Click **Deploy site**

4. **Your site is live!**
   - Netlify will provide a URL like: `https://random-name-123456.netlify.app`
   - You can customize this URL in Site settings

### Custom Domain on Netlify
- Go to **Domain settings**
- Add your custom domain
- Follow the DNS configuration instructions

---

## Option 3: Vercel

Vercel is another excellent platform for static sites.

### Steps:

1. **Create a Vercel account:**
   - Go to https://vercel.com
   - Sign up with your GitHub account

2. **Import your project:**
   - Click **Add New...** → **Project**
   - Select **Import Git Repository**
   - Choose your `Web-Dev-Portfoilio-` repository

3. **Configure project:**
   - Framework Preset: **Other** (or leave as detected)
   - Root Directory: Leave as `./`
   - Build Command: Leave empty
   - Output Directory: Leave as `./`
   - Click **Deploy**

4. **Your site is live!**
   - Vercel will provide a URL like: `https://web-dev-portfoilio.vercel.app`
   - Your site will auto-deploy on every push to your repository

---

## Option 4: Local Testing

To test your website locally before deploying:

### Method 1: Using Python (Recommended)
If you have Python installed:

```bash
# Navigate to your project directory
cd Web-Dev-Portfoilio-

# Python 3
python -m http.server 8000

# Or Python 2
python -m SimpleHTTPServer 8000
```

Then open http://localhost:8000 in your browser.

### Method 2: Using Node.js
If you have Node.js installed:

```bash
# Install http-server globally
npm install -g http-server

# Navigate to your project directory
cd Web-Dev-Portfoilio-

# Start the server
http-server -p 8000
```

Then open http://localhost:8000 in your browser.

### Method 3: Using VS Code Live Server
If you use Visual Studio Code:
1. Install the "Live Server" extension
2. Right-click on `index.html`
3. Select "Open with Live Server"
4. Your default browser will open with the site

### Method 4: Direct File Open
Simply open `index.html` in your web browser:
- Right-click on `index.html`
- Choose "Open with" and select your browser
- Note: Some features may not work with the `file://` protocol

---

## Recommended: GitHub Pages

For this portfolio, **GitHub Pages** is recommended because:
- ✅ Free and easy to set up
- ✅ Your code is already on GitHub
- ✅ Automatic HTTPS
- ✅ Good performance
- ✅ Easy to update (just push to GitHub)

---

## Troubleshooting

### Site not loading correctly
- Check that `index.html` is in the root directory
- Verify all CSS files are in the `css/` folder
- Ensure all image paths are correct
- Check browser console for errors (F12)

### CSS not loading
- Make sure file paths in `index.html` are correct
- Check that CSS files exist in the `css/` directory
- Verify the `global.css` file is in the root directory

### Images not showing
- Confirm images are in the `images/` folder
- Check image file names match exactly (case-sensitive)
- Verify image paths in HTML and CSS

---

## Need Help?

If you encounter any issues:
1. Check the hosting platform's documentation
2. Review browser console errors (F12)
3. Verify all file paths are correct
4. Make sure all files are committed and pushed to GitHub

Happy deploying! 🚀
