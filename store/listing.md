# Google Play listing: Trust Issues

Everything below is ready to paste into Play Console. Character limits are Google's current limits (check the console if a field rejects text).

## Store listing > Main store listing

**App name** (30 max)
```
Trust Issues: Troll Platformer
```

**Short description** (80 max)
```
54 trick levels where floors, spikes and doors lie. Can you reach the exit?
```

**Full description** (4000 max)
```
Trust Issues is a cartoon troll platformer about a tiny sprout-headed hero who just wants to reach the door.

The problem: nothing in these levels is honest.

• Floors crumble the second you trust them
• Spikes pop out of empty ground
• Ceiling blocks drop at the worst moment
• Doors run away, and some doors are fake
• Invisible platforms hold you up, if you can find them
• Sometimes your controls flip

HOW IT PLAYS
Move left and right, and jump. Every level is a short, suspicious dash to the exit. You will die. Restarts are instant, so you learn the trick and go again.

FEATURES
• 54 levels in three chapters, with new tricks every few stages: bounce pads, blinking stones, timed spikes, reversing controls, patrolling prickles and more
• Heartbreak Peak: 14 much harder levels, with collectible hearts hidden in the risky spots
• Earn up to 3 stars on every level, and keep an eye out for a very happy ending
• 23 different cartoon explosions. Every time you die it goes off in a new way: fireworks, confetti, a mushroom cloud, a burst of hearts...
• Stuck on a level? Skip it after a few tries
• Level select, so you can replay your favourites
• A wardrobe for your hero: colours and hats, some earned with stars and hearts, the rest one-time purchases
• Stuck? Watch an optional ad to skip a level. Ads only ever show when you ask for one
• Big touch controls made for phones
• Plays offline (the internet is only used for ads and purchases)
• No accounts, no sign-in

Think you can handle 54 levels of lies?
```

**App icon**: `store/icon-512.png` (512 x 512)
**Feature graphic**: `store/feature-graphic-1024x500.png` (1024 x 500)
**Phone screenshots** (min 2, up to 8): everything in `store/screenshots/` (1080 x 1920 each, portrait)

## Store settings

| Field | Value |
|---|---|
| App or game | Game |
| Category | Arcade (tag it Platformer, Casual) |
| Free or paid | Free (with in-app purchases and optional rewarded ads) |
| Contact email | your public support email |
| Privacy policy URL | `https://muhammadrafay78.github.io/Trust-Issues/privacy.html` (see below) |
| Target audience | 13 and over (avoids the stricter Families rules; the game is not designed for young children) |
| Ads | **Contains ads** (optional rewarded ads only) |

## Privacy policy page (free hosting)

The policy is in `docs/privacy.html`.
1. Open `docs/privacy.html` and replace `CONTACT-EMAIL-HERE` with an email you are happy to show publicly.
2. On GitHub: Settings > Pages > Build and deployment > Deploy from a branch > `main` / `/docs` > Save.
3. After a minute the page is live at the URL in the table above. Open it once to check, then paste it into Play Console.

## App content answers (Play Console > Policy and programs > App content)

**Data safety** (confirm each answer in the console against the AdMob SDK disclosure)
- Does your app collect or share any of the required user data types? **Yes**
- Data types: **Device or other IDs** (advertising ID), collected and shared with Google AdMob for **Advertising or marketing**. Collection is required for ads to work and is not optional per user, but ads are only shown if the player chooses to watch one.
- Is all data encrypted in transit? **Yes**
- Can users request deletion? Game progress is stored only on the device and is removed on uninstall. Advertising ID can be reset or deleted in Android settings.
- Purchases are processed by Google Play. The app does not collect payment info or purchase history itself.
- The game saves progress, stars, hearts and owned cosmetics on the device only.

**Content rating (IARC questionnaire)**
Answer honestly. Expect these answers:
- Violence: cartoon characters are comically defeated by spikes, explosions and similar. Pick the mild cartoon or fantasy violence option, with no realistic violence, no blood, no gore.
- Sexual content, profanity, drugs, gambling: none.
- User-generated content, chat, location sharing: none.
- Digital purchases: **yes** (cosmetic items). Ads: **yes** (optional rewarded video).
Google assigns the final rating from your answers.

**Ads**: Yes, contains ads (rewarded video via AdMob, opt-in).
**In-app products**: create the products listed in the README section "Ads and purchases" (all one-time, non-consumable).
**News app, COVID, government, financial features**: No.

## Release notes (first release)
```
First release: 54 levels of trust issues.
```

## Before you can publish (checklist)
- [ ] Signing key created and GitHub secrets added (`KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`)
- [ ] Release bundle (`.aab`) downloaded from the GitHub Actions run
- [ ] Package name `com.muhammadrafay.trustissues` confirmed (it cannot be changed after the first upload)
- [ ] Privacy policy live and contact email filled in
- [ ] AdMob app created, real app id in `android/app/src/main/res/values/strings.xml`, real rewarded ad unit id in `MONEY.rewardedAdId` and `MONEY.adsTest` set to `false` in `www/index.html`
- [ ] In-app products created in Play Console (ids in the README), and tested with a licence-tester account
- [ ] Play Developer account verified. New personal accounts may need a closed test with about 12 testers for 14 days before production (check the current rule in the console)
