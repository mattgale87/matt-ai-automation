# Portfolio Website Deployment Guide

## Platform Comparison Summary

Based on research, here are the best **FREE** options for hosting your single-page portfolio:

### 1. **Carrd (Free Tier)** ⭐ Best for Non-Technical Users
- **Free tier limits**: 3 sites max, basic elements only
- **Custom domain**: ❌ Pro required ($9/year)
- **Ease of use**: ⭐⭐⭐⭐⭐ Extremely easy, drag-and-drop
- **Professional appearance**: ⭐⭐⭐⭐ Clean templates
- **Gotchas**: 
  - Shows "Made with Carrd" branding on free tier
  - Limited to one-page sites (perfect for your use case)
  - No custom code on free tier

### 2. **GitHub Pages** ⭐⭐ Best Overall (Recommended)
- **Free tier limits**: Unlimited sites, 1GB storage, 100GB/month bandwidth
- **Custom domain**: ✅ Yes, with free SSL
- **Ease of use**: ⭐⭐⭐ Requires Git knowledge
- **Professional appearance**: ⭐⭐⭐⭐⭐ Full control over design
- **Gotchas**: 
  - Static sites only (perfect for your HTML)
  - Need to use Git for updates
  - URL: `yourusername.github.io`

### 3. **Netlify (Free Tier)** ⭐⭐ Excellent Alternative
- **Free tier limits**: 300 credits/month (~100GB bandwidth), unlimited sites
- **Custom domain**: ✅ Yes, with free SSL
- **Ease of use**: ⭐⭐⭐⭐ Drag-and-drop or Git integration
- **Professional appearance**: ⭐⭐⭐⭐⭐ Full control
- **Gotchas**: 
  - Credit system can be confusing
  - Sites pause if you exceed limits (rare for small sites)

### 4. **Vercel (Free Tier)** ⭐⭐ Great for Developers
- **Free tier limits**: Unlimited sites, 100GB bandwidth/month
- **Custom domain**: ✅ Yes, with free SSL
- **Ease of use**: ⭐⭐⭐⭐ Git-based or CLI
- **Professional appearance**: ⭐⭐⭐⭐⭐ Full control
- **Gotchas**: 
  - Optimized for Next.js but works with static HTML
  - Commercial use restrictions on free tier (check ToS)

### 5. **Google Sites** ⭐ Good for Google Users
- **Free tier limits**: Unlimited sites, 15GB storage (shared with Google Drive)
- **Custom domain**: ✅ Only with Google Workspace (paid)
- **Ease of use**: ⭐⭐⭐⭐⭐ Very easy
- **Professional appearance**: ⭐⭐⭐ Limited templates
- **Gotchas**: 
  - URL: `sites.google.com/view/yoursite`
  - Less professional look
  - Limited customization

### 6. **Notion (Public Page)** ⭐ Minimal Option
- **Free tier limits**: Unlimited pages
- **Custom domain**: ❌ Requires third-party tools (Sotion, Super.so - paid)
- **Ease of use**: ⭐⭐⭐⭐⭐ If you know Notion
- **Professional appearance**: ⭐⭐ Looks like a Notion page
- **Gotchas**: 
  - Not a real website builder
  - URL is long and ugly without paid tools
  - Limited design control

### 7. **Cloudflare Pages** ⭐ Hidden Gem
- **Free tier limits**: Unlimited sites, 100GB bandwidth/month
- **Custom domain**: ✅ Yes, with free SSL
- **Ease of use**: ⭐⭐⭐ Git-based
- **Professional appearance**: ⭐⭐⭐⭐⭐ Full control
- **Gotchas**: 
  - Newer platform, less documentation
  - Requires Git workflow

---

## 🏆 Recommendation: GitHub Pages

**Why GitHub Pages is best for your portfolio:**
- ✅ Completely free, no credit card required
- ✅ Custom domain support with free SSL
- ✅ Professional, no branding
- ✅ Perfect for static HTML sites
- ✅ Reliable and fast (hosted on GitHub's infrastructure)
- ✅ Easy updates via Git

---

## Deployment Instructions

### Option A: GitHub Pages (Recommended)

#### Prerequisites
- GitHub account (free at github.com)
- Git installed on your computer

#### Step 1: Create a GitHub Repository
1. Go to https://github.com/new
2. Repository name: `portfolio` (or `matt-ai-automation`)
3. Make it **Public**
4. Click "Create repository"

#### Step 2: Upload Your Site

**Method 1: Using Git (Recommended)**
```bash
cd /Users/matt/.openclaw/workspace/business-setup/portfolio
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
git push -u origin main
```

**Method 2: Using GitHub Web Interface**
1. Go to your repository on GitHub
2. Click "Add file" → "Upload files"
3. Drag and drop `index.html`
4. Click "Commit changes"

#### Step 3: Enable GitHub Pages
1. Go to your repository → Settings → Pages
2. Under "Source", select "Deploy from a branch"
3. Branch: `main`, Folder: `/ (root)`
4. Click "Save"
5. Wait 1-2 minutes for deployment

#### Step 4: Access Your Site
Your site will be live at:
```
https://YOUR_USERNAME.github.io/portfolio/
```

#### Step 5 (Optional): Add Custom Domain
1. Buy a domain (Namecheap, Google Domains, etc.)
2. In GitHub Pages settings, add your custom domain
3. Update DNS records at your domain registrar:
   - Type: `A`, Name: `@`, Value: `185.199.108.153`
   - Type: `A`, Name: `@`, Value: `185.199.109.153`
   - Type: `A`, Name: `@`, Value: `185.199.110.153`
   - Type: `A`, Name: `@`, Value: `185.199.111.153`
   - Type: `CNAME`, Name: `www`, Value: `YOUR_USERNAME.github.io`
4. Enable "Enforce HTTPS" in GitHub Pages settings

---

### Option B: Netlify (Easiest, No Git Required)

#### Step 1: Create Netlify Account
1. Go to https://www.netlify.com/
2. Sign up for free (no credit card needed)

#### Step 2: Deploy Your Site
**Method 1: Drag and Drop**
1. Log into Netlify
2. Go to "Sites" → "Add new site" → "Deploy manually"
3. Drag the `portfolio` folder to the upload area
4. Wait for deployment (~30 seconds)

**Method 2: Git Integration**
1. "Add new site" → "Import an existing project"
2. Connect your GitHub account
3. Select your portfolio repository
4. Deploy settings:
   - Build command: (leave blank)
   - Publish directory: `/` or `portfolio`
5. Click "Deploy site"

#### Step 3: Access Your Site
Your site will be live at:
```
https://random-name-12345.netlify.app
```

#### Step 4 (Optional): Customize Domain
1. Go to Site settings → Domain management
2. Click "Add custom domain"
3. Follow DNS setup instructions
4. Enable HTTPS (automatic)

---

### Option C: Vercel

#### Step 1: Create Vercel Account
1. Go to https://vercel.com/
2. Sign up with GitHub (recommended) or email

#### Step 2: Deploy
1. Click "Add New" → "Project"
2. Import your GitHub repository OR drag-and-drop folder
3. Framework Preset: "Other"
4. Click "Deploy"

#### Step 3: Access Your Site
```
https://your-project.vercel.app
```

---

## Updating Your Site

### GitHub Pages
```bash
# Edit index.html, then:
git add .
git commit -m "Updated services/pricing"
git push
```
Changes go live in 1-2 minutes.

### Netlify (Drag & Drop)
1. Go to your site dashboard
2. Click "Deploys" → "Deploy manually"
3. Upload updated folder

### Netlify/Vercel (Git)
Push to your repository; auto-deploys on every commit.

---

## Quick Checklist

- [ ] Choose hosting platform (GitHub Pages recommended)
- [ ] Create account
- [ ] Upload `index.html`
- [ ] Verify site is live
- [ ] Update contact info in `index.html`:
  - Email address
  - Phone number
  - LinkedIn profile
- [ ] (Optional) Add custom domain
- [ ] (Optional) Add analytics (Google Analytics, Plausible)
- [ ] Test on mobile devices
- [ ] Share your portfolio!

---

## Tips for Success

1. **Update Contact Info**: Edit the email, phone, and LinkedIn links in `index.html` before deploying.

2. **Add Real Case Studies**: Replace the placeholder case studies with actual projects you've completed.

3. **Consider Analytics**: Add Google Analytics or Plausible (privacy-friendly) to track visitors.

4. **SEO Basics**: 
   - Add meta description in `<head>`
   - Consider adding Open Graph tags for social sharing
   - Submit sitemap to Google Search Console

5. **Performance**: The current HTML is already optimized (no external dependencies, inline CSS).

6. **Backup**: Keep a copy of your files locally and in a Git repository.

---

## Need Help?

- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **Netlify Docs**: https://docs.netlify.com
- **Vercel Docs**: https://vercel.com/docs

---

**Your portfolio is ready to go! 🚀**
