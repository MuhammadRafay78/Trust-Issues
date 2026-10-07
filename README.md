# So Close

A one-tap rage-bait mobile game. Built with plain HTML canvas (`www/index.html`) and packaged for Android with Capacitor.

## Build
CI (`.github/workflows/build.yml`) builds a debug APK on every push to `main`. Add these repo secrets to also get a signed Play Store bundle: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`.

Local: `npm ci && npx cap sync android && cd android && ./gradlew assembleDebug` (needs JDK 21 and the Android SDK).
