# Trust Issues

A troll platformer for phones. Reach the door on each of 54 levels in three chapters (the last, Heartbreak Peak, is the hard one). Floors, spikes, ceilings and doors lie to you, and every death is a different cartoon explosion. Fog hides what is coming (only a few tiles ahead are visible), and every level can be opened from the level select. Earn up to 3 stars per level and collect the hearts hidden in the hard levels.

Plain HTML canvas (`www/index.html`), packaged for Android (landscape) with Capacitor.

## Build
CI (`.github/workflows/build.yml`) builds a debug APK on every push to `main`. Add these repo secrets to also get a signed Play Store bundle: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`.

Local: `npm ci && npx cap sync android && cd android && ./gradlew assembleDebug` (needs JDK 21 and the Android SDK).

Package name is `com.muhammadrafay.trustissues`. It cannot change after the first Play upload.

## Ads and purchases
Both are built in and use Google's own test setup until you plug in your accounts.

**Rewarded ads (skip a level).** After 3 deaths on a level the player can watch an ad to skip it (AdMob, with the consent form where required). Today it uses Google's public test ids, so only test ads ever show. Before the Play release:
1. Create an app in AdMob and a *Rewarded* ad unit.
2. Put the AdMob **app id** in `android/app/src/main/res/values/strings.xml` (`admob_app_id`).
3. In `www/index.html`, set `MONEY.rewardedAdId` to your ad unit id and `MONEY.adsTest` to `false`.

**Mascot wardrobe (colours and hats).** Some items unlock with stars or hearts. The rest are one-time purchases through Google Play Billing. In Play Console > Monetise > In-app products, create these (non-consumable, a price each; `bundle_all` unlocks every paid item):
`color_sky`, `color_grape`, `color_gold`, `color_midnight`, `hat_catears`, `hat_shades`, `hat_wizard`, `hat_tophat`, `hat_halo`, `bundle_all`.
Prices shown in the game come from Play, so set them there. Test with a licence-tester account on an internal-testing build.

In a plain browser (no app) the ad is a 3 second preview and purchases just unlock, so the web version is for testing only.

## Store assets
`store/` has the Play Store icon, feature graphic, screenshots and the full listing text (`store/listing.md`). `docs/privacy.html` is the privacy policy page (publish it with GitHub Pages: Settings > Pages > `main` / `/docs`).
