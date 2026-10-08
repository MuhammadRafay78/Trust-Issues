# Trust Issues

A troll platformer for phones. Reach the door on each of 8 levels. Floors, spikes, ceilings and doors lie to you.

Plain HTML canvas (`www/index.html`), packaged for Android (landscape) with Capacitor.

## Build
CI (`.github/workflows/build.yml`) builds a debug APK on every push to `main`. Add these repo secrets to also get a signed Play Store bundle: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`.

Local: `npm ci && npx cap sync android && cd android && ./gradlew assembleDebug` (needs JDK 21 and the Android SDK).

Package name `com.trustissues.game` is a placeholder. Change it before the first Play upload; it cannot change afterwards.

## Store assets
`store/` has the Play Store icon, feature graphic, screenshots and the full listing text (`store/listing.md`). `docs/privacy.html` is the privacy policy page (publish it with GitHub Pages: Settings > Pages > `main` / `/docs`).
