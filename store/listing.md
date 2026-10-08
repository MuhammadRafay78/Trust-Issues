# Google Play listing: Trust Issues

Everything below is ready to paste into Play Console. Character limits are Google's current limits (check the console if a field rejects text).

## Store listing > Main store listing

**App name** (30 max)
```
Trust Issues: Troll Platformer
```

**Short description** (80 max)
```
40 trick levels where floors, spikes and doors lie. Can you reach the exit?
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
• 40 levels, with new tricks every few stages: bounce pads, blinking stones, timed spikes, reversing controls and more
• 20 different cartoon deaths. You might melt, blast off, get squashed by an anvil or be abducted by a UFO
• Stuck on a level? Skip it after a few tries
• Level select, so you can replay your favourites
• Big touch controls made for phones
• Works fully offline
• No ads, no accounts, no data collected

Think you can handle 40 levels of lies?
```

**App icon**: `store/icon-512.png` (512 x 512)
**Feature graphic**: `store/feature-graphic-1024x500.png` (1024 x 500)
**Phone screenshots** (min 2, up to 8): everything in `store/screenshots/` (1920 x 960 each)

## Store settings

| Field | Value |
|---|---|
| App or game | Game |
| Category | Arcade (tag it Platformer, Casual) |
| Free or paid | Free |
| Contact email | your public support email |
| Privacy policy URL | `https://muhammadrafay78.github.io/Trust-Issues/privacy.html` (see below) |
| Target audience | 13 and over (avoids the stricter Families rules; the game is not designed for young children) |
| Ads | No ads |

## Privacy policy page (free hosting)

The policy is in `docs/privacy.html`.
1. Open `docs/privacy.html` and replace `CONTACT-EMAIL-HERE` with an email you are happy to show publicly.
2. On GitHub: Settings > Pages > Build and deployment > Deploy from a branch > `main` / `/docs` > Save.
3. After a minute the page is live at the URL in the table above. Open it once to check, then paste it into Play Console.

## App content answers (Play Console > Policy and programs > App content)

**Data safety**
- Does your app collect or share any of the required user data types? **No**
- The game saves the furthest level reached on the device only, and sends nothing off the device. It makes no network requests (the font is embedded).

**Content rating (IARC questionnaire)**
Answer honestly. Expect these answers:
- Violence: cartoon characters are comically defeated by spikes, explosions and similar. Pick the mild cartoon or fantasy violence option, with no realistic violence, no blood, no gore.
- Sexual content, profanity, drugs, gambling: none.
- User-generated content, chat, location sharing, purchases: none.
Google assigns the final rating from your answers.

**Ads**: No ads.
**News app, COVID, government, financial features**: No.

## Release notes (first release)
```
First release: 40 levels of trust issues.
```

## Before you can publish (checklist)
- [ ] Signing key created and GitHub secrets added (`KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, `KEY_PASSWORD`)
- [ ] Release bundle (`.aab`) downloaded from the GitHub Actions run
- [ ] Package name `com.trustissues.game` confirmed (it cannot be changed after the first upload)
- [ ] Privacy policy live and contact email filled in
- [ ] Play Developer account verified. New personal accounts may need a closed test with about 12 testers for 14 days before production (check the current rule in the console)
