# C2 Android App

This repository builds an installable Android APK named **C2**.

- Application ID: `com.c2.companion`
- Minimum Android: API 24 (Android 7.0)
- Target SDK: 34
- Build: Android Gradle Plugin 8.5.2, Gradle 8.7, JDK 17
- Runtime: Android WebView shell loading https://avatar-talkie.lovable.app/
- Native bridge: Android microphone permission handling

## Build

Pushes to `main` or `master` and manual workflow dispatch run the GitHub Actions workflow **Build C2 APK**.

The workflow builds and verifies:
`app/build/outputs/apk/debug/app-debug.apk`

It uploads the installable APK as the workflow artifact **C2-APK**.

## Important limitation

This is a WebView wrapper around the live C2 website, not a full native rewrite. An internet connection is required. Website features and data are served by the live website.
