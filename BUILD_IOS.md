# Building Crew List Scanner for iPhone

The app is the same Crew List Scanner page, wrapped with Capacitor (like the
Iingwane logbook). Everything, including the passport/ID reader, is bundled
inside the app, so scanning works offline at sea.

## What you need (one time)

1. **Xcode** from the Mac App Store. Open it once and let it install its extras.
   Your MacBook is an Intel model: the current Xcode needs a recent macOS, so if
   the App Store won't install it, check *Apple menu → About This Mac* and update
   macOS first.
2. **Node.js** (you already have nvm): `nvm install 22 && nvm use 22`
3. **An Apple ID** signed in to Xcode (*Xcode → Settings → Accounts*).
   - Free Apple ID: installs on your own iPhone, but the app stops opening after 7 days and must be re-installed from Xcode.
   - Apple Developer Program (US$99/year): needed for skippers' phones via TestFlight or the App Store.

## Build and run on your iPhone

```bash
cd ~/Documents/Programs/GitHub/crew-list-app
npm install
npx cap sync ios
npx cap open ios
```

In Xcode:

1. Click **App** (blue icon, top of the left sidebar) → **Signing & Capabilities**.
2. Tick **Automatically manage signing** and choose your **Team** (your Apple ID).
3. If it complains the bundle ID is taken, change `com.johannkruger.crewlist` to something unique.
4. Plug in your iPhone with a cable, unlock it, and pick it at the top of the Xcode window.
5. Press **▶ Run**.
6. First time only, on the iPhone: *Settings → General → VPN & Device Management* → trust your developer profile.
   On iOS 16+ also turn on *Settings → Privacy & Security → Developer Mode*.

## After changing the app

Edit `www/index.html`, then:

```bash
npx cap sync ios
```

and press ▶ Run in Xcode again.

## Android build from the same code

```bash
npx cap sync android
npx cap open android      # then Build → Build APK(s) in Android Studio
```

## Getting it onto skippers' iPhones

With the paid developer account: in Xcode choose *Product → Archive → Distribute App → TestFlight*.
Skippers install the free TestFlight app and you invite them by email. No App Store review is needed for internal testers.
