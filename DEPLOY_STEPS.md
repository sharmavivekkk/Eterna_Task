# Clean Deployment Steps for Vercel

## 📋 Pre-Deployment Checklist

### Step 1: Verify Build Locally
```bash
# Clean install dependencies
rm -rf node_modules package-lock.json
npm install

# Run build to check for errors
npm run build

# Test production build locally
npm start
```
Visit `http://localhost:3000` and verify everything works.

### Step 2: Clean Up Files
```bash
# Remove unnecessary files (if any)
# Make sure .gitignore includes:
# - .next/
# - node_modules/
# - .vercel/
# - .env.local
```

### Step 3: Commit All Changes
```bash
# Check git status
git status

# Add all files
git add .

# Commit with descriptive message
git commit -m "feat: Complete Axiom Trade replica with chart and trading panel"
```

---

## 🚀 Deployment Methods

### Method 1: GitHub + Vercel Dashboard (Recommended)

#### Step 1: Push to GitHub
```bash
# Initialize git (if not already done)
git init

# Add remote repository (create one on GitHub first)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

#### Step 2: Deploy on Vercel
1. Go to [vercel.com](https://vercel.com)
2. Sign in with GitHub
3. Click **"Add New..."** → **"Project"**
4. Import your GitHub repository
5. Vercel will auto-detect:
   - Framework: Next.js
   - Build Command: `npm run build`
   - Output Directory: `.next`
6. Click **"Deploy"**
7. Wait for deployment to complete (usually 2-3 minutes)

#### Step 3: Get Your Live URL
- Your site will be live at: `https://your-project-name.vercel.app`
- Vercel provides a production URL automatically

---

### Method 2: Vercel CLI (Alternative)

#### Step 1: Install Vercel CLI
```bash
npm i -g vercel
```

#### Step 2: Login to Vercel
```bash
vercel login
```
This will open a browser for authentication.

#### Step 3: Deploy
```bash
# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

Follow the prompts:
- Set up and deploy? **Yes**
- Which scope? **Your account**
- Link to existing project? **No** (first time) or **Yes** (if updating)
- Project name? **Enter a name or press Enter for default**
- Directory? **Press Enter** (current directory)

---

## ✅ Post-Deployment Verification

### Step 1: Test Live Site
1. Visit your Vercel URL
2. Test all features:
   - ✅ Token discovery table loads
   - ✅ Clicking tokens navigates to detail page
   - ✅ Chart displays and is interactive
   - ✅ Trading panel works
   - ✅ Responsive design on mobile/tablet/desktop
   - ✅ All buttons and interactions work

### Step 2: Check Build Logs
1. Go to Vercel Dashboard
2. Click on your project
3. Check **"Deployments"** tab
4. Verify build was successful (green checkmark)

### Step 3: Test Responsive Design
- Open browser DevTools (F12)
- Test different viewport sizes:
  - Mobile: 320px, 375px, 414px
  - Tablet: 768px, 1024px
  - Desktop: 1280px, 1920px

---

## 🔧 Troubleshooting

### Build Fails
1. Check build logs in Vercel dashboard
2. Common issues:
   - **TypeScript errors**: Run `npm run build` locally first
   - **Missing dependencies**: Ensure all are in `package.json`
   - **Node version**: Vercel uses Node 18+ by default

### Site Doesn't Load
1. Check deployment status in Vercel dashboard
2. Verify build completed successfully
3. Check browser console for errors
4. Verify all routes are working

### Environment Variables (if needed later)
1. Go to Vercel Dashboard → Your Project → Settings → Environment Variables
2. Add any required variables
3. Redeploy after adding variables

---

## 📝 Quick Reference Commands

```bash
# Local development
npm run dev

# Build locally
npm run build

# Test production build
npm start

# Lint check
npm run lint

# Type check
npm run type-check

# Deploy via CLI
vercel --prod
```

---

## 🎯 Deployment Checklist

- [ ] Build passes locally (`npm run build`)
- [ ] Production build works (`npm start`)
- [ ] All changes committed to git
- [ ] Pushed to GitHub (if using Method 1)
- [ ] Deployed on Vercel
- [ ] Live site tested and working
- [ ] Responsive design verified
- [ ] All features functional

---

## 🔗 Useful Links

- **Vercel Dashboard**: https://vercel.com/dashboard
- **Vercel Docs**: https://vercel.com/docs
- **Next.js Deployment**: https://nextjs.org/docs/deployment

---

## 💡 Pro Tips

1. **Automatic Deployments**: Every push to `main` branch auto-deploys to production
2. **Preview Deployments**: Other branches create preview URLs for testing
3. **Custom Domain**: Add your domain in Vercel Dashboard → Settings → Domains
4. **Analytics**: Enable Vercel Analytics in project settings for performance insights

---

**Your site is now live! 🎉**

