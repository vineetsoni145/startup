# GitHub Deployment Guide

This guide will help you deploy your Farmish website to GitHub and make it live using GitHub Pages.

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in the details:
   - **Repository name**: `farmish-website` (or any name you prefer)
   - **Description**: "Modern 3D website for organic farm delivery"
   - **Visibility**: Choose Public (required for free GitHub Pages)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. Click **"Create repository"**

## Step 2: Connect Local Repository to GitHub

After creating the repository, GitHub will show you commands. Use these commands in your terminal:

### Option A: If you haven't pushed yet (First time)

```bash
cd "C:\Users\VINEET SONI\OneDrive\Desktop\Startup Farmish"
git remote add origin https://github.com/YOUR_USERNAME/farmish-website.git
git branch -M main
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username!**

### Option B: If repository already exists on GitHub

```bash
cd "C:\Users\VINEET SONI\OneDrive\Desktop\Startup Farmish"
git remote add origin https://github.com/YOUR_USERNAME/farmish-website.git
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **"Settings"** tab (top menu)
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **"Save"**

## Step 4: Access Your Live Website

After a few minutes, your website will be live at:
```
https://YOUR_USERNAME.github.io/farmish-website/
```

**Note**: It may take 5-10 minutes for the site to be available initially.

## Step 5: (Optional) Rename HTML File

If you want `example.html` to be the default page, you have two options:

### Option A: Rename to index.html (Recommended)
```bash
cd "C:\Users\VINEET SONI\OneDrive\Desktop\Startup Farmish"
git mv example.html index.html
git commit -m "Rename example.html to index.html for GitHub Pages"
git push
```

### Option B: Keep example.html
Your site will be accessible at:
```
https://YOUR_USERNAME.github.io/farmish-website/example.html
```

## Future Updates

Whenever you make changes to your website:

```bash
cd "C:\Users\VINEET SONI\OneDrive\Desktop\Startup Farmish"
git add .
git commit -m "Description of your changes"
git push
```

Changes will automatically update on GitHub Pages within a few minutes.

## Troubleshooting

### Issue: "remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/farmish-website.git
```

### Issue: Authentication required
You may need to:
1. Use a Personal Access Token instead of password
2. Or use GitHub Desktop for easier authentication

### Issue: Pages not showing
1. Check that repository is Public (not Private)
2. Wait 5-10 minutes after enabling Pages
3. Check the Pages settings in repository Settings

## Custom Domain (Optional)

If you have a custom domain:

1. Go to repository Settings → Pages
2. Enter your custom domain
3. Add a `CNAME` file in your repository root with your domain name
4. Update your domain's DNS settings as instructed by GitHub

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Community Forum](https://github.community/)

---

**Quick Command Reference:**

```bash
# Navigate to project
cd "C:\Users\VINEET SONI\OneDrive\Desktop\Startup Farmish"

# Check status
git status

# Add all changes
git add .

# Commit changes
git commit -m "Your commit message"

# Push to GitHub
git push

# Pull latest changes
git pull
```

