# 🌿 AyurvedaGPT PWA Setup Guide

Your app is now configured as a Progressive Web App (PWA)! This means users can install it on any device like a native app.

## ✅ What's Been Configured

1. **Web App Manifest** - Defines how your app appears when installed
2. **Service Worker** - Enables offline functionality and faster loading
3. **PWA Icons** - Custom icons for different devices
4. **Install Prompt** - Users will see an "Install App" button
5. **Standalone Mode** - Runs in its own window (no browser UI)

## 🚀 How to Run the PWA

### Option 1: Development Mode (Testing)

```bash
cd frontend
npm run web
```

Then open in your browser:
- Local: http://localhost:8081
- On your phone: http://YOUR_IP:8081

### Option 2: Production Build (For Deployment)

```bash
cd frontend

# Build for production
npm run build

# Test the build locally
npm run serve
```

This creates an optimized build in the `web-build` folder.

## 📱 How to Install the PWA

### On Desktop (Chrome/Edge):
1. Open the app in your browser
2. Look for the "Install" icon in the address bar (or "Install App" button on the page)
3. Click it and confirm
4. The app will open in its own window!

### On Mobile (Android):
1. Open the app in Chrome
2. Tap the menu (⋮) and select "Install app" or "Add to Home screen"
3. The app icon will appear on your home screen
4. Tap it to launch the app

### On iOS (iPhone/iPad):
1. Open the app in Safari
2. Tap the Share button (📤)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"

## 🌐 Deploying Your PWA

You can deploy your PWA to any hosting service:

### Option 1: Netlify (Free & Easy)

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Build the app
cd frontend
npm run build

# Deploy
netlify deploy --dir=web-build --prod
```

### Option 2: Vercel

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
cd frontend
npm run build
vercel --prod
```

### Option 3: GitHub Pages

1. Build the app: `npm run build`
2. Push the `web-build` folder to a GitHub repository
3. Enable GitHub Pages in repository settings
4. Set source to the `web-build` folder

### Option 4: Any Static Host

Just upload the contents of the `web-build` folder to:
- Firebase Hosting
- AWS S3 + CloudFront
- Cloudflare Pages
- Your own server

## 🎨 Customizing Icons

The current icons are simple SVG placeholders. For better branding:

1. Create proper PNG icons (192x192 and 512x512)
2. Replace the SVG files in `public/` folder
3. Update `manifest.json` to reference PNG files
4. See `public/ICONS_README.md` for detailed instructions

## 🔧 PWA Features

Your app now supports:

- ✅ **Offline Access** - Works even without internet
- ✅ **Fast Loading** - Cached resources load instantly
- ✅ **Installable** - Add to home screen on any device
- ✅ **Standalone Mode** - Runs like a native app
- ✅ **Auto Updates** - Service worker updates automatically
- ✅ **Mobile Responsive** - Works on phones, tablets, desktop

## 📊 Testing Your PWA

### Chrome DevTools Lighthouse:
1. Open your app in Chrome
2. Press F12 to open DevTools
3. Go to "Lighthouse" tab
4. Check "Progressive Web App"
5. Click "Generate report"

### PWA Checklist:
- [ ] Manifest file is valid
- [ ] Service worker is registered
- [ ] HTTPS is enabled (required for production)
- [ ] Icons are present
- [ ] Responsive design works
- [ ] Offline functionality works

## 🔐 Important Notes

**For Production:**
- You MUST use HTTPS (required for service workers)
- Most free hosting services provide HTTPS automatically
- Test on multiple devices before launching

**Backend Configuration:**
- Update the API_URL in your screens to point to your production backend
- Ensure CORS is configured to allow requests from your PWA domain

## 🎉 Next Steps

1. Build the production version: `npm run build`
2. Deploy to a hosting service (Netlify/Vercel recommended)
3. Share the URL with users
4. Users can install it as an app on their devices!

## 💡 Tips

- The install prompt appears automatically when PWA criteria are met
- Users can always install from browser menu if they miss the prompt
- Test on real mobile devices for best experience
- Consider adding push notifications in the future
- Monitor with Google Analytics or similar tools

---

**Need Help?**
- PWA Documentation: https://web.dev/progressive-web-apps/
- Expo Web: https://docs.expo.dev/workflow/web/
- Service Workers: https://developers.google.com/web/fundamentals/primers/service-workers

Enjoy your installable AyurvedaGPT PWA! 🌿📱
