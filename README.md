# Drumwell Tempo

Android WebView app and GitHub Pages version of the uploaded Drumwell Tempo Library.

## What's included
- `index.html` — browser version for GitHub Pages.
- `app/` — Android Studio project that packages the same app as an APK.
- Song Library and Setlists are stored locally on the device/browser using `localStorage`. No online database or account sync is configured.

## Publish the website
1. Create a new **public** GitHub repository.
2. Upload all files and folders in this project to the repository root (not just the ZIP).
3. Open **Settings → Pages** and choose **GitHub Actions** as the deployment source.
4. The `Publish GitHub Pages` workflow will publish `index.html`.

## Build the Android APK on GitHub
1. Push the project to the repository's `main` branch.
2. Open the repository's **Actions** tab.
3. Select **Build Android APK** and wait for the workflow to finish.
4. Open the completed workflow run, scroll to **Artifacts**, and download `DrumwellTempo-debug-apk`.
5. Extract the downloaded artifact ZIP; install `app-debug.apk` on your Android phone. You may need to allow installation from your browser/file manager.

## Build locally
Open this folder in Android Studio and build the `app` module, or run `gradle assembleDebug` with Android SDK installed.

## Data note
Saved songs and setlists are offline/local to the browser or app installation. They do not automatically sync between devices. Clearing app data or uninstalling the app may erase the locally saved data. Export/backup is not currently included.
