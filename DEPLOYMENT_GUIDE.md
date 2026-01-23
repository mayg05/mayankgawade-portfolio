# Deployment Guide - Free GitHub Pages

This guide will walk you through deploying your portfolio website to GitHub Pages for **FREE** - no domain purchase needed!

## Prerequisites

- GitHub account (you already have one)
- Git installed on your computer

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Repository name: `MayankPortfolio` or `mayankgawade-portfolio`
5. Description: "Personal Portfolio Website"
6. Make it **Public** (required for free GitHub Pages)
7. **DO NOT** initialize with README, .gitignore, or license (we already have these)
8. Click "Create repository"

## Step 2: Push Your Code to GitHub

Open your terminal/command prompt in the project directory and run:

```bash
# Stage all files
git add .

# Create initial commit
git commit -m "Initial commit: Portfolio website"

# Add GitHub remote (replace [username] with your GitHub username)
git remote add origin https://github.com/[username]/MayankPortfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Note**: If you're asked for credentials, use a Personal Access Token instead of password.

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** (top menu)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select:
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for deployment
7. Your site will be available at: `https://[username].github.io/MayankPortfolio`

**That's it!** Your website is now live and accessible to anyone on the internet.

## Step 4: Verify Deployment

1. Visit `https://[username].github.io/MayankPortfolio` in your browser
2. Test all functionality:
   - Navigation links
   - Download buttons (resume, certifications)
   - Contact form
   - Mobile responsiveness
   - All sections load correctly

## Troubleshooting

### 404 Error
- Verify the repository is **public** (required for free GitHub Pages)
- Check that GitHub Pages is enabled in Settings > Pages
- Ensure you're using the correct branch (main/master)
- Wait a few minutes after enabling Pages for the first deployment

### Site not updating
- GitHub Pages can take 1-2 minutes to rebuild after each push
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check the Actions tab in your repository to see deployment status

### HTTPS not working
- GitHub Pages automatically provides HTTPS for all sites
- If you see a warning, wait a few minutes for the SSL certificate to provision
- Make sure you're accessing the site via `https://` not `http://`

## Alternative Deployment Options (Also Free!)

### Netlify (Alternative to GitHub Pages)

1. Go to [Netlify](https://www.netlify.com)
2. Sign up/login (free)
3. Drag and drop your project folder, OR
4. Connect your GitHub repository for automatic deployments
5. Your site will be live at: `https://[random-name].netlify.app`

**Advantages**: Faster deployment, better performance, automatic HTTPS

### Vercel (Alternative to GitHub Pages)

1. Go to [Vercel](https://vercel.com)
2. Sign up/login with GitHub (free)
3. Import your GitHub repository
4. Your site will be live at: `https://[project-name].vercel.app`

**Advantages**: Excellent performance, automatic deployments, great for static sites

## Post-Deployment Checklist

- [ ] Site loads at the GitHub Pages URL
- [ ] HTTPS is enabled and working (automatic on GitHub Pages)
- [ ] All navigation links work
- [ ] Resume download works
- [ ] Certification downloads work
- [ ] Contact form validation works
- [ ] Mobile responsive design works
- [ ] All images and assets load correctly
- [ ] Tested on multiple browsers (Chrome, Firefox, Safari, Edge)

## Updating Your Website

After making changes to your website:

```bash
# Stage changes
git add .

# Commit changes
git commit -m "Description of changes"

# Push to GitHub
git push origin main
```

GitHub Pages will automatically rebuild and deploy your site within 1-2 minutes. No additional steps needed!

## Customizing Your URL

If you want a shorter URL, you can:

1. Rename your repository to match your GitHub username
   - If your username is `mayg05`, name the repo `mayg05.github.io`
   - Your site will be at: `https://mayg05.github.io` (no repository name needed)

2. Or use a different repository name for a custom subdomain
   - Example: `portfolio` → `https://[username].github.io/portfolio`

## Support

If you encounter any issues:
1. Check GitHub Pages documentation: [docs.github.com/pages](https://docs.github.com/pages)
2. Verify repository is public
3. Check repository Settings > Pages
4. Review browser console for errors
5. Check the Actions tab for deployment logs

---

**Congratulations!** Your portfolio is now live on the internet for free! 🚀
