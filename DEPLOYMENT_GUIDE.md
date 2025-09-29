# 🚀 Deployment Guide for Maro Kurukshetram News

## Prerequisites
- Node.js 22.x or higher
- npm or yarn package manager
- Vercel account (free tier available)

## Quick Deployment Steps

### 1. **Prepare Your Project**
```bash
# Install dependencies
npm install

# Test build locally
npm run build

# Test preview
npm run preview
```

### 2. **Deploy to Vercel**

#### Option A: Vercel CLI (Recommended)
```bash
# Install Vercel CLI globally
npm i -g vercel

# Login to Vercel
vercel login

# Deploy from project directory
vercel

# Follow the prompts:
# - Set up and deploy? Yes
# - Which scope? (select your account)
# - Link to existing project? No
# - What's your project's name? marokurukshetram-news
# - In which directory is your code located? ./
```

#### Option B: GitHub Integration
1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Vercel will auto-detect Vite configuration

### 3. **Environment Variables Setup**

In your Vercel dashboard, go to Project Settings > Environment Variables and add:

```
API_BASE_URL = https://phpstack-1520234-5847937.cloudwaysapps.com/api/v1
VITE_API_BASE_URL = https://phpstack-1520234-5847937.cloudwaysapps.com/api/v1
```

### 4. **Verify Deployment**

After deployment, check:
- ✅ Homepage loads correctly
- ✅ Language switching works
- ✅ News pages load
- ✅ API calls work (check browser network tab)
- ✅ Mobile responsiveness

## Troubleshooting

### Common Issues & Solutions

#### 1. **Build Fails**
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
npm run build
```

#### 2. **API Calls Fail**
- Check environment variables in Vercel dashboard
- Verify API_BASE_URL is set correctly
- Check browser console for CORS errors

#### 3. **Routing Issues**
- Ensure vercel.json has correct rewrites
- Check that all routes are defined in App.tsx

#### 4. **Static Assets Not Loading**
- Check that public folder is included
- Verify asset paths in build output

### 5. **Performance Issues**
- Enable Vercel Analytics
- Check bundle size in build output
- Consider code splitting for large components

## Production Checklist

- [ ] Environment variables configured
- [ ] Build completes without errors
- [ ] All routes work correctly
- [ ] API integration functional
- [ ] Mobile responsive
- [ ] Error boundaries working
- [ ] i18n translations working
- [ ] Performance optimized

## Support

If you encounter issues:
1. Check Vercel deployment logs
2. Review browser console errors
3. Test locally with `npm run preview`
4. Verify environment variables

## Advanced Configuration

### Custom Domain
1. Go to Project Settings > Domains
2. Add your custom domain
3. Configure DNS records as instructed

### Analytics
1. Enable Vercel Analytics in project settings
2. Monitor performance and errors

### Edge Functions (Optional)
For better performance, consider moving API routes to Edge Functions.

---

**Happy Deploying! 🎉**
