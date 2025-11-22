# 🚀 GitHub Pages Setup Guide

## ✅ Your Code is Ready!

All your portfolio files have been:
- ✅ Committed to git
- ✅ Pushed to GitHub
- ✅ Ready for deployment

Branch: `claude/resume-analysis-tool-01Kv3YaztrBaUfGjq5pbBK7c`

---

## 📋 Enable GitHub Pages (2 Minutes)

### Step 1: Go to Your Repository

Visit: **https://github.com/Tayyab-dv/portfolio**

### Step 2: Open Settings

1. Click the **"Settings"** tab (top right of repository page)
2. Look for **"Pages"** in the left sidebar
3. Click **"Pages"**

### Step 3: Configure Source

Under **"Build and deployment"**:

1. **Source**: Select **"Deploy from a branch"**
2. **Branch**: Click the dropdown and select:
   - Branch: `claude/resume-analysis-tool-01Kv3YaztrBaUfGjq5pbBK7c`
   - Folder: `/ (root)`
3. Click **"Save"**

### Step 4: Wait for Deployment

- GitHub will start building your site
- This takes **2-5 minutes**
- You'll see a blue banner saying "GitHub Pages source saved"
- Refresh the page after a few minutes

### Step 5: Get Your URL

Once deployed, you'll see:

```
✅ Your site is live at https://tayyab-dv.github.io/portfolio/
```

---

## 🎯 Access Your Live Site

Once deployed, visit:

- **Homepage**: https://tayyab-dv.github.io/portfolio/
- **Resume Analyzer**: https://tayyab-dv.github.io/portfolio/resume-analyzer.html

---

## 🧪 Test Your Deployment

### 1. Homepage Test
- [ ] Visit homepage
- [ ] Check Resume Analyzer card appears
- [ ] Click "Launch Tool →"
- [ ] Verify navigation works

### 2. Resume Analyzer Test
- [ ] Page loads correctly
- [ ] "Back to Portfolio" link works
- [ ] File upload inputs are visible
- [ ] API key field is present

### 3. Full Function Test
Get an Anthropic API key from: https://console.anthropic.com/

- [ ] Upload `sample-resume.txt`
- [ ] Paste `sample-job-description.txt` content
- [ ] Enter API key
- [ ] Click "Analyze"
- [ ] Verify results appear (takes 10-30 seconds)

---

## 📸 Screenshots Guide

### Finding Settings → Pages

```
GitHub Repository Page
├── Code
├── Issues
├── Pull requests
├── Actions
├── Projects
├── Wiki
├── Security
├── Insights
└── Settings ← Click here
    └── Pages ← Click here (in left sidebar)
```

### Pages Configuration

```
GitHub Pages
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Build and deployment

Source
  Deploy from a branch ← Select this

Branch
  [Select branch ▼] claude/resume-analysis-tool-01Kv3YaztrBaUfGjq5pbBK7c
  [Select folder ▼] / (root)

  [Save] ← Click this
```

---

## 🔧 Troubleshooting

### Issue: Can't find Settings tab

**Solution**:
- Make sure you're logged into GitHub
- Verify you have admin access to the repository
- Settings tab is on the top navigation bar

### Issue: Branch not showing in dropdown

**Solution**:
- Refresh the GitHub page
- Verify branch exists: https://github.com/Tayyab-dv/portfolio/branches
- The branch name is: `claude/resume-analysis-tool-01Kv3YaztrBaUfGjq5pbBK7c`

### Issue: 404 Error when visiting site

**Solution**:
- Wait 5 minutes after enabling (initial build takes time)
- Check if deployment completed: Settings → Pages
- Verify URL is exactly: `https://tayyab-dv.github.io/portfolio/`
- Try hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

### Issue: Site loads but Resume Analyzer doesn't work

**Solution**:
- Check browser console for errors (F12)
- Verify you have a valid Anthropic API key
- Make sure you're using HTTPS URL (not HTTP)

### Issue: Deployment failed

**Solution**:
- Check Actions tab for build errors
- Ensure all files are valid HTML
- Try disabling and re-enabling GitHub Pages

---

## 🔄 Updating Your Site

Every time you push new changes to the branch, GitHub Pages will automatically rebuild and deploy!

**To update:**
```bash
# Make your changes
git add .
git commit -m "Your update message"
git push
```

Wait 2-3 minutes, and your changes will be live!

---

## 🎨 Custom Domain (Optional)

Want to use your own domain like `yourname.com`?

### Steps:

1. **In GitHub Pages Settings:**
   - Enter your domain in "Custom domain" field
   - Click "Save"

2. **In Your Domain Registrar (GoDaddy, Namecheap, etc.):**

   Add these DNS records:

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

   Type: CNAME
   Name: www
   Value: tayyab-dv.github.io
   ```

3. **Wait for DNS propagation** (can take up to 48 hours)
4. **Enable "Enforce HTTPS"** in GitHub Pages settings

---

## 📊 Monitor Your Site

### Check Deployment Status
Visit: https://github.com/Tayyab-dv/portfolio/deployments

### View Build Logs
Visit: https://github.com/Tayyab-dv/portfolio/actions

---

## 🎉 You're Done!

Once you complete the steps above, your portfolio will be live on the internet!

**Share your live URL:**

```
🚀 Check out my AI Tools Portfolio!

Portfolio: https://tayyab-dv.github.io/portfolio/
Resume Analyzer: https://tayyab-dv.github.io/portfolio/resume-analyzer.html

Built with React, Tailwind CSS, and Claude AI.
```

---

## 💡 Pro Tips

- GitHub Pages is **100% free** for public repositories
- Includes **free SSL certificate** (HTTPS)
- Updates **automatically** when you push to the branch
- Served from **GitHub's global CDN** (fast worldwide)
- No bandwidth limits for reasonable usage

---

## 📞 Need Help?

- **GitHub Pages Docs**: https://docs.github.com/pages
- **Check Deployment Status**: https://github.com/Tayyab-dv/portfolio/deployments
- **Community Forum**: https://github.community

Your portfolio is ready to go live - just follow the steps above! 🎊
