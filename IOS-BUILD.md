# Build Lumina for iPhone (GitHub Actions)

1. Paste the whole contents of this repo into a new GitHub repo (keep the `.github` folder).
2. Actions tab -> **Build iOS (unsigned IPA)** -> **Run workflow** (about 10-15 min).
3. Download the **lumina-ios-unsigned-ipa** artifact (a zip containing `Lumina-unsigned.ipa`).
4. The IPA is unsigned. Install it with AltStore or Sideloadly (needs a computer once and a free Apple ID),
   or sign it in CI with an Apple Developer account for TestFlight.

The Android workflow (`build-apk.yml`) is unchanged. The iOS workflow is manual-only because
macOS runner minutes count 10x on private repos.

iPhone notes: AVPlayer cannot play MKV or some codecs, so modules that return those links will fail on iPhone.
