# Zavi Locator — Android APK + Windows EXE

This package is based on the supplied `markhor-locator` repository. The existing Markhor `www/index.html` has been replaced with the supplied Zavi Locator HTML, including its embedded BTS dataset. Original uploaded repository ZIP is not modified.

## Build Android APK
1. Upload/commit these files to `https://github.com/zakirshar-151/markhor-locator` on the `main` branch.
2. Open **Actions**.
3. Run **Build Zavi Locator APK** manually (`workflow_dispatch`) or push changes to `main`.
4. Open the successful workflow run and download artifact **Zavi-Locator-APK**.
5. Extract the downloaded artifact ZIP; install `app-debug.apk` on Android.

## Build Windows EXE
1. In Actions, run **Build Zavi Locator Windows Installer** manually, or push changes affecting `www/index.html` / `desktop/**`.
2. Download artifact **Zavi-Locator-Windows-Installer** from the completed run.

## Important
- This builds a debug APK for testing, not a Play Store signed release.
- The HTML is a large file with an embedded dataset. Keep the full file when uploading; do not edit it in a text editor that truncates large files.
- Supabase backend/authentication must be tested on-device after the build. A publishable Supabase key can be present in client HTML, but service-role/secret keys must never be placed in HTML.
- This setup uses `www/index.html` as the shared app source, so the resulting Android and Windows installers both launch Zavi Locator, not the previous Markhor HTML.
