# Deployment Guide

Quick guide to deploy your portfolio to various platforms.

## 🌐 Deployment Options

### Option 1: GitHub Pages (Free)

**Steps:**
1. Push code to GitHub repository
2. Go to repository Settings
3. Navigate to "Pages" section
4. Under "Source", select your branch (e.g., `main`)
5. Select folder: `/ (root)`
6. Click Save
7. Wait 2-3 minutes for deployment
8. Your site will be live at: `https://<username>.github.io/<repo-name>/`

**Pros:**
- Free hosting
- Automatic SSL
- Direct integration with GitHub
- Custom domain support

**Cons:**
- Public repositories only (for free)
- Limited build minutes

---

### Option 2: Netlify (Recommended)

**Steps:**
1. Create account at [netlify.com](https://netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Connect to your Git provider (GitHub, GitLab, Bitbucket)
4. Select your repository
5. Build settings:
   - **Build command:** (leave empty)
   - **Publish directory:** `/` or `.`
6. Click "Deploy site"
7. Site will be live at: `https://<random-name>.netlify.app`
8. Optional: Add custom domain in Site Settings

**Pros:**
- Free tier available
- Automatic deployments on git push
- Custom domains with SSL
- Form handling & serverless functions
- `netlify.toml` config included

**Cons:**
- Free tier has bandwidth limits

**Custom Domain:**
1. Go to Site Settings → Domain Management
2. Click "Add custom domain"
3. Enter your domain name
4. Update DNS records with your provider:
   ```
   Type: A
   Name: @
   Value: 75.2.60.5

   Type: CNAME
   Name: www
   Value: <your-site>.netlify.app
   ```

---

### Option 3: Vercel

**Steps:**
1. Create account at [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import Git repository
4. Configure:
   - **Framework Preset:** Other
   - **Build Command:** (leave empty)
   - **Output Directory:** (leave empty)
5. Click "Deploy"
6. Site will be live at: `https://<project-name>.vercel.app`

**Pros:**
- Fast global CDN
- Automatic HTTPS
- Instant deployments
- Great analytics
- `vercel.json` config included

**Cons:**
- Free tier has execution limits

---

### Option 4: Cloudflare Pages

**Steps:**
1. Login to [Cloudflare](https://dash.cloudflare.com)
2. Go to "Pages"
3. Click "Create a project"
4. Connect to Git
5. Select repository
6. Build settings:
   - **Build command:** (leave empty)
   - **Build output directory:** `/`
7. Click "Save and Deploy"
8. Site will be live at: `https://<project-name>.pages.dev`

**Pros:**
- Unlimited bandwidth (free tier)
- Fast global network
- Built-in analytics
- DDoS protection

**Cons:**
- Slightly more complex setup

---

### Option 5: Firebase Hosting

**Steps:**
1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```

2. Login to Firebase:
   ```bash
   firebase login
   ```

3. Initialize project:
   ```bash
   firebase init hosting
   ```

4. Configure:
   - Select or create Firebase project
   - Public directory: `.` (current directory)
   - Configure as single-page app: `No`
   - Set up automatic builds: `No`

5. Deploy:
   ```bash
   firebase deploy --only hosting
   ```

6. Site will be live at: `https://<project-id>.web.app`

**Pros:**
- Google infrastructure
- Generous free tier
- Easy rollbacks

**Cons:**
- Requires CLI tool
- More setup steps

---

## ⚙️ Configuration Files

Your repository includes:

- **`netlify.toml`** - Netlify configuration
- **`vercel.json`** - Vercel configuration
- **`.gitignore`** - Files to ignore in git

## 🔒 Environment Variables

For the Resume Analyzer, users will need to:
1. Get an Anthropic API key from [console.anthropic.com](https://console.anthropic.com/)
2. Enter it in the tool's interface

**No server-side environment variables needed** - all API calls are client-side.

## 🎯 Custom Domain Setup

### General Steps (most platforms):

1. Purchase domain from registrar (Namecheap, GoDaddy, etc.)
2. In your hosting platform, add custom domain
3. Update DNS records at your registrar:

**For apex domain (example.com):**
```
Type: A
Name: @
Value: [provided by hosting platform]
```

**For www subdomain:**
```
Type: CNAME
Name: www
Value: [your-site].[platform].app
```

4. Wait for DNS propagation (5 minutes - 48 hours)
5. Platform will auto-provision SSL certificate

## ✅ Post-Deployment Checklist

After deploying, verify:

- [ ] Homepage (`index.html`) loads correctly
- [ ] Resume Analyzer link works
- [ ] Resume Analyzer page loads
- [ ] File upload functionality works
- [ ] API key input works
- [ ] Sample files can be downloaded
- [ ] Navigation between pages works
- [ ] Mobile responsive design works
- [ ] HTTPS is enabled
- [ ] No console errors

## 🐛 Troubleshooting

### Issue: Pages not loading

**Solution:**
- Check build logs
- Verify all files are committed and pushed
- Ensure `index.html` is in root directory

### Issue: API calls failing

**Solution:**
- Check browser console for CORS errors
- Verify API key is valid
- Check Anthropic API status

### Issue: Files not found (404)

**Solution:**
- Ensure file paths are relative (not absolute)
- Check file names match exactly (case-sensitive)
- Verify files are committed to repository

### Issue: Styles not loading

**Solution:**
- Check Tailwind CDN is accessible
- Verify CSP headers allow CDN resources
- Check browser console for errors

## 📊 Monitoring

Once deployed, you can monitor:

- **Netlify:** Built-in analytics in dashboard
- **Vercel:** Analytics tab in project
- **Cloudflare:** Pages Analytics
- **GitHub Pages:** GitHub Insights

## 🔄 Continuous Deployment

All platforms support automatic deployments:

1. Make changes locally
2. Commit to git: `git add . && git commit -m "Update"`
3. Push to GitHub: `git push`
4. Platform automatically rebuilds and deploys
5. Changes live in 1-5 minutes

## 💰 Cost Comparison

| Platform | Free Tier | Bandwidth | Builds/Month | Custom Domain |
|----------|-----------|-----------|--------------|---------------|
| GitHub Pages | ✅ | 100GB | Unlimited | ✅ |
| Netlify | ✅ | 100GB | 300 min | ✅ |
| Vercel | ✅ | 100GB | 100 hrs | ✅ |
| Cloudflare | ✅ | Unlimited | 500/month | ✅ |
| Firebase | ✅ | 10GB | Unlimited | ✅ |

All options are **free for this static site**.

## 🚀 Quick Deploy Buttons

Add these to your README for one-click deployment:

**Netlify:**
```markdown
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/YOUR_USERNAME/YOUR_REPO)
```

**Vercel:**
```markdown
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/YOUR_REPO)
```

---

**Need help?** Check platform-specific documentation:
- [GitHub Pages Docs](https://docs.github.com/pages)
- [Netlify Docs](https://docs.netlify.com)
- [Vercel Docs](https://vercel.com/docs)
- [Cloudflare Pages Docs](https://developers.cloudflare.com/pages)
