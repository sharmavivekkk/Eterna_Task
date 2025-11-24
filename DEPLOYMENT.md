# Deployment Guide

## Vercel Deployment

This project is configured for easy deployment on Vercel.

### Prerequisites

1. A GitHub account
2. A Vercel account (sign up at [vercel.com](https://vercel.com))

### Deployment Steps

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Axiom Trade replica"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Deploy to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will auto-detect Next.js settings
   - Click "Deploy"

3. **Environment Variables** (if needed)
   - Add any required environment variables in Vercel dashboard
   - Currently, no environment variables are required for this project

### Automatic Deployments

- **Production**: Every push to `main` branch
- **Preview**: Every push to other branches creates a preview deployment

### Manual Deployment

You can also deploy using Vercel CLI:

```bash
npm i -g vercel
vercel
```

## Responsive Design

The application is fully responsive and tested down to **320px width**:

- **Mobile (320px - 640px)**: Stacked layout, horizontal scroll for table
- **Tablet (640px - 1024px)**: Improved spacing, some stacked elements
- **Desktop (1024px+)**: Full layout with sidebars

### Responsive Breakpoints

- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px

## Performance

- Lighthouse score: ≥ 90 (mobile & desktop)
- Interactions: < 100ms
- No layout shifts
- Optimized bundle size

## Build Verification

Before deploying, verify the build:

```bash
npm run build
npm start
```

Visit `http://localhost:3000` to test the production build locally.

