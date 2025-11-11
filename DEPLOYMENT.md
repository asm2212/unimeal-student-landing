# 🚀 Deployment Guide - Unimeal Student Landing Page

This landing page is designed to be publicly accessible so users can freely download the Unimeal Student App, even when the main app repository is private.

## 📋 Overview

The landing page serves as a **public download portal** for the Unimeal Student App, allowing users to:
- View app features and information
- Download the APK directly via button or QR code
- Access app documentation and support

## 🌐 Deployment Options

### Option 1: Vercel (Recommended) ⚡

**Status**: ✅ Configured and Ready

#### Quick Deploy to Vercel:

1. **Via Vercel Dashboard** (Easiest):
   - Go to [vercel.com/new](https://vercel.com/new)
   - Import `asm2212/unimeal-student-landing` repository
   - Click "Deploy"
   - Done! Your site will be live at `https://unimeal-student-landing.vercel.app`

2. **Via Vercel CLI**:
   ```bash
   npm install -g vercel
   cd /home/oro/dev/unimeal/unimeal-student-landing
   vercel
   ```

#### Configuration:
- ✅ `vercel.json` configured
- ✅ Build command: Creates `public/` directory
- ✅ Output directory: `public/`
- ✅ Auto-deploys on git push

### Option 2: GitHub Pages 📄

**Status**: ✅ Already Deployed

- **Live URL**: https://asm2212.github.io/unimeal-student-landing/
- **Auto-deploys**: On every push to master branch
- **Workflow**: `.github/workflows/deploy.yml`

No additional setup needed - already working!

### Option 3: Netlify 🎯

#### Quick Deploy:

1. **Drag & Drop**:
   - Go to [app.netlify.com/drop](https://app.netlify.com/drop)
   - Drag the `unimeal-student-landing` folder
   - Done!

2. **Via Git**:
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click "New site from Git"
   - Select GitHub → `unimeal-student-landing`
   - Build settings:
     - Build command: `npm run build`
     - Publish directory: `public`
   - Deploy!

### Option 4: Custom Server 🖥️

Deploy to your own server:

```bash
# Copy files to server
scp -r * user@yourserver.com:/var/www/unimeal-landing/

# Or use rsync
rsync -avz --exclude 'node_modules' --exclude '.git' \
  . user@yourserver.com:/var/www/unimeal-landing/
```

Configure your web server (nginx/apache) to serve the files.

## 🔗 Download Link Configuration

### Current Setup:

The landing page links to the **public GitHub release**:
```
https://github.com/asm2212/unimeal-student-app/releases/download/v1.4.0/unimeal-v1.4.0.apk
```

### If Main Repo is Private:

You have several options:

#### Option A: Keep Releases Public (Recommended)
Even if your repository is private, you can make releases public:
1. Go to repository Settings → General
2. Scroll to "Danger Zone"
3. Keep releases public while repo is private

#### Option B: Host APK on Landing Page
1. Add APK to landing page repository:
   ```bash
   cd /home/oro/dev/unimeal/unimeal-student-landing
   mkdir -p downloads
   cp /path/to/unimeal-v1.4.0.apk downloads/
   ```

2. Update download links in `index.html`:
   ```html
   <a href="./downloads/unimeal-v1.4.0.apk" class="btn-primary" download>
   ```

3. Update QR code URL:
   ```html
   <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://asm2212.github.io/unimeal-student-landing/downloads/unimeal-v1.4.0.apk">
   ```

#### Option C: Use Cloud Storage
Upload APK to:
- **Google Drive** (make link public)
- **Dropbox** (create public link)
- **AWS S3** (configure public bucket)
- **Firebase Storage** (set public rules)

Then update the download URL in `index.html`.

## 📱 QR Code Updates

The QR code is dynamically generated using QR Server API:

```html
<img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=YOUR_DOWNLOAD_URL">
```

To update:
1. Replace `YOUR_DOWNLOAD_URL` with your APK URL
2. Commit and push changes
3. QR code will automatically update

## 🔄 Updating the Landing Page

### Update App Version:

1. Edit `index.html`:
   - Update version badge
   - Update download links
   - Update "What's New" section

2. Commit and push:
   ```bash
   git add .
   git commit -m "Update to version X.X.X"
   git push origin master
   ```

3. All deployments will auto-update!

### Update Styling:

Edit `style.css` and push changes. All platforms will auto-deploy.

## 🔒 Security Considerations

### For Private Repository:

1. **Never commit sensitive data** to landing page repo
2. **Use environment variables** for any API keys
3. **Keep APK download links public** but repository private
4. **Monitor download analytics** to track usage

### Best Practices:

- ✅ Landing page repository: **Public**
- ✅ Main app repository: **Can be Private**
- ✅ APK releases: **Public** (or hosted separately)
- ✅ Source code: **Private** (in main repo)

## 📊 Analytics (Optional)

Add Google Analytics or Plausible to track:
- Page views
- Download clicks
- User locations
- Device types

Add to `index.html` before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🎯 Custom Domain (Optional)

### For Vercel:
1. Go to Project Settings → Domains
2. Add your custom domain (e.g., `download.unimeal.app`)
3. Update DNS records as instructed

### For GitHub Pages:
1. Add `CNAME` file with your domain
2. Update DNS records
3. Enable HTTPS in repository settings

### For Netlify:
1. Go to Domain Settings
2. Add custom domain
3. Follow DNS instructions

## ✅ Deployment Checklist

- [x] Landing page created
- [x] GitHub repository created (public)
- [x] GitHub Pages enabled and deployed
- [x] Vercel configuration added
- [ ] Choose primary deployment platform
- [ ] Configure custom domain (optional)
- [ ] Add analytics (optional)
- [ ] Test download links
- [ ] Test QR code
- [ ] Share URL with users!

## 🔗 Live URLs

- **GitHub Pages**: https://asm2212.github.io/unimeal-student-landing/
- **Vercel**: Deploy to get URL (e.g., `unimeal-student-landing.vercel.app`)
- **Repository**: https://github.com/asm2212/unimeal-student-landing

## 📞 Support

For deployment issues:
- Email: asmareadmasu0@gmail.com
- GitHub Issues: https://github.com/asm2212/unimeal-student-landing/issues

---

**Made with ❤️ for Students - Unimeal v1.4.0**
