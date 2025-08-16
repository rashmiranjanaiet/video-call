# Deployment Guide

This guide covers multiple deployment options for the LoveLink dating website.

## 🚀 Quick Deploy Options

### 1. GitHub Pages (Recommended)

**Automatic Deployment:**
1. Fork/clone this repository
2. Update `package.json` homepage URL with your GitHub username
3. Update `vite.config.ts` base path with your repository name
4. Push to GitHub
5. Enable GitHub Pages in repository settings
6. Select "GitHub Actions" as source

**Manual Deployment:**
```bash
npm run deploy:github
```

### 2. Netlify

**Option A: Drag & Drop**
1. Run `npm run build`
2. Drag the `dist` folder to Netlify

**Option B: Git Integration**
1. Connect your GitHub repository
2. Build command: `npm run build`
3. Publish directory: `dist`

### 3. Vercel

**Option A: CLI**
```bash
npm i -g vercel
npm run build
vercel --prod
```

**Option B: Git Integration**
1. Connect GitHub repository
2. Build command: `npm run build`
3. Output directory: `dist`

### 4. Firebase Hosting

```bash
npm install -g firebase-tools
npm run build
firebase login
firebase init hosting
firebase deploy
```

### 5. Surge.sh

```bash
npm install -g surge
npm run build
cd dist
surge
```

## 🔧 Build Configuration

### Environment Variables

Create `.env` file for local development:
```env
VITE_APP_TITLE=LoveLink
VITE_API_URL=https://api.lovelink.com
```

### Custom Base Path

For subdirectory deployment, update `vite.config.ts`:
```typescript
export default defineConfig({
  base: '/your-subdirectory/',
  // ... other config
});
```

## 📋 Pre-deployment Checklist

- [ ] Update repository URLs in `package.json`
- [ ] Update base path in `vite.config.ts` if needed
- [ ] Test build locally: `npm run build && npm run preview`
- [ ] Check all links and navigation work
- [ ] Verify responsive design on different devices
- [ ] Test all interactive features
- [ ] Ensure all images load correctly

## 🐛 Common Issues

### Build Fails
```bash
# Clear cache and reinstall
npm run clean
rm -rf node_modules package-lock.json
npm install
npm run build
```

### 404 on Page Refresh
This is normal for SPAs. Configure your hosting provider:

**Netlify:** Create `public/_redirects`:
```
/*    /index.html   200
```

**Apache:** Create `public/.htaccess`:
```apache
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.html [L]
```

### Images Not Loading
- Ensure all image URLs are absolute or properly relative
- Check image paths in production build
- Verify CORS settings for external images

## 🔒 Security Considerations

### HTTPS
Always deploy with HTTPS enabled. Most modern hosting providers offer this by default.

### Environment Variables
Never commit sensitive data. Use environment variables for:
- API keys
- Database URLs
- Third-party service credentials

### Content Security Policy
Consider adding CSP headers for enhanced security:
```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src 'self' https:; script-src 'self';">
```

## 📊 Performance Optimization

### Build Optimization
The project includes several optimizations:
- Code splitting
- Tree shaking
- Asset optimization
- Gzip compression

### CDN Integration
For better performance, consider using a CDN:
- Cloudflare
- AWS CloudFront
- Google Cloud CDN

## 🔄 Continuous Deployment

### GitHub Actions (Included)
The project includes a GitHub Actions workflow that:
- Runs on every push to main
- Installs dependencies
- Runs type checking and linting
- Builds the project
- Deploys to GitHub Pages

### Custom CI/CD
For other platforms, adapt the workflow:
```yaml
- name: Build
  run: npm run build
  
- name: Deploy
  run: your-deploy-command
```

## 📈 Monitoring

### Analytics
Add analytics to track usage:
- Google Analytics
- Plausible
- Fathom Analytics

### Error Tracking
Consider error tracking services:
- Sentry
- LogRocket
- Bugsnag

## 🆘 Support

If you encounter deployment issues:
1. Check the build logs for errors
2. Verify all dependencies are installed
3. Test the build locally first
4. Check hosting provider documentation
5. Open an issue on GitHub

## 📚 Additional Resources

- [Vite Deployment Guide](https://vitejs.dev/guide/static-deploy.html)
- [React Deployment Guide](https://create-react-app.dev/docs/deployment/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Netlify Documentation](https://docs.netlify.com/)
- [Vercel Documentation](https://vercel.com/docs)