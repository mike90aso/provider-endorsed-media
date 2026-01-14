# Deployment Setup Guide

This guide will help you connect your Provider Endorsed Media website to GitHub and Netlify for automatic deployments.

## Step 1: Configure Git (if not already done)

```bash
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

## Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `provider-endorsed-media` (or your preferred name)
3. **Don't** initialize it with a README, .gitignore, or license
4. Copy the repository URL (e.g., `https://github.com/yourusername/provider-endorsed-media.git`)

## Step 3: Connect Local Repository to GitHub

Run these commands in your terminal:

```bash
cd /Users/michaelmcgahey/provider-endorsed-media
git add .
git commit -m "Initial commit - Provider Endorsed Media website"
git branch -M main
git remote add origin https://github.com/yourusername/provider-endorsed-media.git
git push -u origin main
```

Replace `yourusername/provider-endorsed-media.git` with your actual GitHub repository URL.

## Step 4: Set Up Netlify

1. Go to [Netlify](https://www.netlify.com) and sign up/login
2. Click "Add new site" → "Import an existing project"
3. Choose "Deploy with GitHub"
4. Authorize Netlify to access your GitHub account
5. Select your `provider-endorsed-media` repository
6. Netlify will auto-detect settings:
   - **Build command:** (leave empty)
   - **Publish directory:** `.` (current directory)
7. Click "Deploy site"

## Step 5: Automatic Deployments

Once connected:
- **Every time you make changes** and I push to GitHub, Netlify will automatically rebuild and deploy your site
- **You can make adjustments** by asking me, and I'll push the changes to GitHub
- **Netlify will deploy** within 1-2 minutes automatically

## Workflow

1. You request changes → I make edits → I push to GitHub → Netlify auto-deploys
2. Your site will be live at: `https://your-site-name.netlify.app`
3. You can add a custom domain in Netlify settings if needed

## Files Included

- `netlify.toml` - Netlify configuration (already set up)
- `.gitignore` - Files to exclude from git (already set up)
- All your website files (index.html, style.css, etc.)

## Need Help?

If you need to make changes:
1. Just tell me what you want changed
2. I'll update the files and push to GitHub
3. Netlify will automatically deploy the changes

