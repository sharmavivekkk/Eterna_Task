# GitHub Repository Setup

## Initial Setup

1. **Initialize Git Repository** (if not already done):
   ```bash
   git init
   ```

2. **Create .gitignore** (already configured):
   - `.next/`
   - `node_modules/`
   - `.env*.local`
   - `dist/`
   - `build/`

3. **Make Initial Commit**:
   ```bash
   git add .
   git commit -m "feat: initial commit - Axiom Trade replica with full responsive design"
   ```

## Clean Commit History

### Commit Message Convention

Use conventional commits for clean history:

- `feat:` - New features
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `perf:` - Performance improvements
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

### Example Commits

```bash
git commit -m "feat: add token discovery table with real-time updates"
git commit -m "feat: implement trading chart with lightweight-charts"
git commit -m "feat: add responsive design support down to 320px"
git commit -m "fix: resolve chart initialization error"
git commit -m "docs: update README with deployment instructions"
git commit -m "refactor: optimize component rendering with memo"
```

## Pushing to GitHub

1. **Create Repository on GitHub**:
   - Go to GitHub and create a new repository
   - Don't initialize with README (we already have one)

2. **Add Remote and Push**:
   ```bash
   git remote add origin https://github.com/yourusername/eterna.git
   git branch -M main
   git push -u origin main
   ```

## Branch Strategy

- `main` - Production-ready code
- `develop` - Development branch (optional)
- `feature/*` - Feature branches
- `fix/*` - Bug fix branches

## Pre-commit Checklist

Before committing, ensure:

- ✅ Code passes TypeScript checks (`npm run type-check`)
- ✅ Code passes ESLint (`npm run lint`)
- ✅ Build succeeds (`npm run build`)
- ✅ No console errors
- ✅ Responsive design tested (320px - 1920px)
- ✅ All features working as expected

## Repository Structure

```
eterna/
├── .github/              # GitHub workflows (optional)
├── app/                  # Next.js app directory
├── components/           # React components
├── docs/                 # Documentation
│   └── responsive-snapshots/  # Layout snapshots
├── hooks/                # Custom hooks
├── lib/                  # Utilities and store
├── scripts/              # Build scripts
├── types/                # TypeScript types
├── .gitignore
├── DEPLOYMENT.md         # Deployment guide
├── GITHUB_SETUP.md       # This file
├── README.md             # Main documentation
└── vercel.json           # Vercel configuration
```

