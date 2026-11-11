# Hazina Android app

This Android project packages the live Hazina web application (`https://hazina.ai.studio`) in a native Android WebView shell. It enables JavaScript, DOM storage and cookies for the web app's login and Firebase-backed flows, supports Android back navigation, and opens non-web links in their matching Android apps.

## Build the APK

### Android Studio
1. Install Android Studio and Android SDK Platform 35.
2. Open this folder (`hazina-android`) in Android Studio.
3. Allow Gradle sync to complete.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK is created at `app/build/outputs/apk/debug/app-debug.apk`.

### GitHub Actions (no local Android SDK required)
1. Create a GitHub repository and upload the contents of this folder.
2. Push to the `main` branch, or open **Actions > Build Hazina APK > Run workflow**.
3. Download the `Hazina-Android-APK` artifact from the completed workflow run.

## Important
- This is a WebView wrapper. The app displays the live website, so an internet connection is required and changes deployed to the website appear in the app.
- The original site controls its own authentication, database access and server-side features. This wrapper does not replace Firebase credentials or backend services.
- The generated debug APK is for testing/sideloading. A Play Store release needs a separately generated, securely stored signing key and a release build.
