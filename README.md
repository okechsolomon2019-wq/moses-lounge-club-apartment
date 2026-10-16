# Moses Lounge Club & Apartment

A responsive, installable website for Moses Lounge in Sukmamur, South Sudan. It is built with plain HTML, CSS, and JavaScript and is published at <https://okechsolomon2019-wq.github.io/>.

## Website deployment

The published website is hosted from the public `okechsolomon2019-wq.github.io` repository. This repository is the app and website source; changes to website files here must also be copied to the Pages repository before they appear at the app's root URL. The existing project Pages URL remains available at <https://okechsolomon2019-wq.github.io/moses-lounge-club-apartment/>.

## Prepare for Google Play

The Android app is configured as a Trusted Web Activity (TWA) for <https://okechsolomon2019-wq.github.io/>. Its package ID is `com.moseslounge.clubapartment`. The public site and privacy policy are live, but the app is not yet signed or submitted. The TWA will display as a browser Custom Tab until the website-to-app Digital Asset Links verification is published.

1. Create and verify the owner's Play Console developer account. Keep account passwords, payment details, and signing keys private; never add them to this repository.
2. Create an upload key in a secure location, enable Play App Signing when prompted, and back up the upload key securely. Never share it or commit it. In a terminal, you can generate one with `keytool -genkeypair -v -keystore android/upload-key.jks -alias moseslounge-upload -keyalg RSA -keysize 2048 -validity 10000`. Choose private passwords and answer the identity prompts yourself.
3. Create the local, ignored `android/keystore.properties` file with `storeFile=../upload-key.jks`, your `storePassword`, `keyAlias=moseslounge-upload`, and your `keyPassword`. Keep both this file and the key out of Git and back them up securely.
4. Build a signed Android App Bundle from `android/` using Android Studio's signed-bundle flow or Gradle. Gradle also accepts the `MOSES_RELEASE_STORE_FILE`, `MOSES_RELEASE_STORE_PASSWORD`, `MOSES_RELEASE_KEY_ALIAS`, and `MOSES_RELEASE_KEY_PASSWORD` environment variables instead of the local properties file. The output is `android/app/build/outputs/bundle/release/app-release.aab`.
5. Create the app in Play Console and upload the AAB to an internal testing release. From Play Console's **App integrity** page, copy the SHA-256 fingerprint for the **App signing key certificate** (not the upload key).
6. Add `/.well-known/assetlinks.json` to the website with package ID `com.moseslounge.clubapartment` and that exact fingerprint, then publish it at <https://okechsolomon2019-wq.github.io/.well-known/assetlinks.json>. Verify the URL returns the JSON successfully before testing the app.
7. Complete the Play listing, privacy policy, content rating, target audience, app access, ads, and data-safety declarations. Test the TWA from Play's internal testing track before requesting production access.

The current site stores account details and booking requests only in the visitor's browser; requests are not sent to the venue and accounts do not sync across devices. Disclose this accurately in Play Console. Google may require additional testing or changes and controls approval and publication. A TWA does not guarantee approval if the app is judged to provide insufficient value beyond the website.

## Android app

An Android TWA project is in `android/`. Pushing Android project changes to `main` runs the **Build Moses Lounge Android app** workflow. On success, the workflow publishes an installable debug APK as a GitHub Release named `android-preview-*`.

To install a preview on Android, open the repository's **Releases** page, download `app-debug.apk`, open the download, and approve Android's “Install unknown apps” prompt for the browser or file manager if Android requests it. This is a test/debug build, not a Play Store release. Android may warn that it is from outside Google Play. Do not install APKs from an unknown source.

The debug APK is for testing only and is not a Play release. A Play release must be built as a signed Android App Bundle with the owner's protected upload key. No signing key or Google credential belongs in this repository.

### Draft Play Store listing

These are draft texts to review and update after live bookings and account handling work end-to-end:

- **App name:** Moses Lounge Sukmamur
- **Short description:** Book rooms, shops, club packages and event spaces in Sukmamur, South Sudan.
- **Full description:** Discover Moses Lounge Club & Apartment in Sukmamur, South Sudan. Explore self-contained rooms, monthly shop rentals, the lounge, conference and party halls, and the club package. Check the published rates and prepare a booking request. Contact manager Mandel Peter by phone to confirm availability. **In this current demo, booking requests and account information stay in the browser on the visitor's device and are not sent to Moses Lounge.** Update this disclosure before the app is submitted if the service changes.
- **Privacy policy URL:** `https://okechsolomon2019-wq.github.io/privacy.html`
- **Support contact:** Mandel Peter, +211 929 994 005 / +211 923 759 776

The listing should not promise confirmed online reservations or working Google sign-in until those features are connected to a secure service. Capture genuine screenshots from the final published app; do not present mockups as app functionality. Complete Play Console content rating, target audience, app access, ads, and data-safety declarations truthfully for the release build. Google's requirements can change; follow the current Play Console prompts.

## Install on a phone or computer

Open the published HTTPS website in Safari on iPhone and use **Share → Add to Home Screen**. In Chrome on Android, use the browser menu and choose **Install app** or **Add to Home screen**. In Chrome or Edge on a computer, use the browser's **Install app** option. The website also keeps its main pages available offline after the first successful visit.

This installs the website as a Progressive Web App (PWA) from the browser. It is not yet an Android Play Store listing or a standalone iPhone App Store application.

## Accounts and booking requests

The email form accepts Gmail addresses as well as other email addresses. The **Continue with Google** button is not active until Google OAuth is configured and Google credentials are verified by a trusted server. Do not treat a Gmail address entered in the email/password form as Google-verified.

This is a front-end demo: account details and booking requests are kept in the current browser's local storage. Accounts and requests do not sync to another phone or computer, and booking requests are not sent to the manager automatically. Customers should call Mandel Peter at **+211 929 994 005** or **+211 923 759 776** to confirm availability.

## Rooms, shops, and facilities

- Self-contained accommodation rooms **1–20**: **50,000 SSP** half day, **100,000 SSP** full day, or **800 USD** monthly.
- Separate shop units **1–15**: **250 USD** monthly.
- Lounge facilities include a swimming pool and pool table. Drinks start at **5,000 SSP**.
- Club booking package: **500 USD**, including **4 bags of water, 6 crates of soda, 1 bottle of Jameson, and 1 bottle of Jack Daniel's**.

Prices are shown as supplied; confirm availability and payment details directly with the manager.

For real multi-device accounts and bookings, connect the site to a trusted server or booking service before collecting customer information. Do not use this local demo as secure production authentication.

## Sample venue photos

The photos in `assets/photos/` are illustrative Unsplash sample images, not photographs of Moses Lounge. They are included locally so the site and its offline PWA cache can display them reliably. Replace them with real venue photos when available. Sources: [guest room](https://images.unsplash.com/photo-1611892440504-42a792e24d32), [rental room](https://images.unsplash.com/photo-1616594039964-ae9021a400a0), [shop](https://images.unsplash.com/photo-1441986300917-64674bd600d8), [club event](https://images.unsplash.com/photo-1470229722913-7c0e2dbbafd3), [lounge](https://images.unsplash.com/photo-1517248135467-4c7edcad34c4), [conference room](https://images.unsplash.com/photo-1497366754035-f200968a6e72), [event hall](https://images.unsplash.com/photo-1519167758481-83f550bb49b3), and [swimming pool](https://images.unsplash.com/photo-1576013551627-0cc20b96c2a7).
