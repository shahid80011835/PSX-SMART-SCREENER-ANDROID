# PSX Smart Screener Android APK project

This Android WebView wrapper opens the existing Streamlit app:
https://psx-smart-screener-2h98ccsfbfexmer34qhvdh.streamlit.app/

## Build APK using GitHub Actions (no Android Studio needed)
1. Create a new GitHub repository, for example `PSX-Smart-Screener-Android`.
2. Upload all files and folders from this project to the repository root. Make sure `.github/workflows/build-apk.yml` is included.
3. Open the repository's **Actions** tab. If GitHub asks, enable workflows.
4. Select **Build PSX Smart Screener APK**, then **Run workflow** (or wait for the first push build).
5. Open the completed green workflow run. Under **Artifacts**, download `PSX-Smart-Screener-APK`.
6. Extract the downloaded artifact ZIP to find `app-debug.apk` and install it on your Android phone. Android may ask you to allow installing unknown apps for the app you used to download it.

## Notes
- This is a debug APK for personal testing, not a Play Store release build.
- Internet access is required. The APK displays the existing Streamlit web app; it does not bundle the Python scanner or make data live by itself.
- The app supports WebView navigation, file chooser and download hand-off, but some website features may behave differently from Chrome. Test upload/download features on the phone.
- The app uses the existing website URL; changing the site URL requires editing `APP_URL` in `MainActivity.java` and rebuilding.
