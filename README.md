# StormPulse app wrapper

Native app shell (Capacitor) that loads https://neon-storm-pulse-live.base44.app

## Build

Requires Node.js 18+. Android needs Android Studio; iOS needs a Mac with Xcode.

    npm install
    npx cap add android      # and/or: npx cap add ios
    npx cap sync
    npx cap open android     # builds/runs in Android Studio (Build > Build APK)
    npx cap open ios         # builds/runs in Xcode

## Notes
- The app needs an internet connection; it displays the live site.
- Change the URL in capacitor.config.json (server.url) if the app moves.
- Add your own icon with: npm i -D @capacitor/assets, put icon.png (1024x1024)
  in an `assets/` folder, then run `npx capacitor-assets generate`.
- Store submissions (especially Apple) may reject thin web wrappers; consider
  exporting the real source from Base44 for a fully bundled build.
