# KEDS Android app

This is an Android WebView wrapper for the KEDS website.

## Website address
The app currently opens:

`https://username4521.github.io/Study-Planner/`

If your published KEDS URL is different, edit `APP_URL` in:
`app/src/main/java/com/keds/studyplanner/MainActivity.java`

## Build an APK using GitHub Actions
1. Upload the contents of this project folder to a GitHub repository (or add them to your existing KEDS repository).
2. Make sure the workflow file `.github/workflows/build-apk.yml` is included.
3. Open the repository on GitHub and select **Actions**.
4. Choose **Build KEDS APK**, then **Run workflow** (or wait for the automatic build after pushing).
5. Open the completed workflow run and download the **KEDS-Android-debug** artifact.
6. Extract the downloaded ZIP. It contains `app-debug.apk`.
7. Transfer `app-debug.apk` to your Android phone and open it to install. Android may ask you to allow installation from that file source.

## Notes
- This is an installable Android APK project, not just an HTML file.
- The app loads the live KEDS website, so an internet connection is required.
- Website features that call backend API endpoints will only work when that backend is deployed and reachable.
- The workflow creates a debug APK for testing. Publishing on Google Play requires a separately signed release build.
