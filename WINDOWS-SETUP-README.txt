MARKHOR LOCATOR — WINDOWS EXE BUILD KIT

This kit adds a Windows installer build to the existing GitHub project. It uses the same shared source file as the Android APK workflow: www/index.html.

INSTALL INTO YOUR EXISTING REPOSITORY
1. Download and extract this ZIP.
2. In your GitHub repository zakirshar-151/markhor-locator, upload the desktop folder, the .github/workflows/build-windows-exe.yml file, and this README.
3. Keep the existing www/index.html and existing Android APK workflow. Do not replace the entire repository with this kit.
4. Commit the changes to the main branch.
5. Open the Actions tab. The Android APK workflow and Windows installer workflow will run separately.
6. Open a successful workflow run and download its artifact:
   - Markhor-Locator-Windows-Installer for the Windows .exe installer
   - Markhor-Locator-APK for the Android APK

SHARED UPDATES
Every time www/index.html is updated on main, both workflows are configured to build from that same HTML source. Windows installer artifacts are build outputs; they are not automatically installed on users' computers. Users need to install the new version when they want to update their Windows app.

IMPORTANT
- This ZIP is the build setup kit, not a prebuilt .exe.
- GitHub Actions builds the .exe on a Windows runner, so no Windows build tools are required on your own PC.
- The app relies on network services/CDNs used by its HTML, so some functions require internet access.
- The existing repository must retain its Android/Capacitor files and its current www/index.html dataset.
