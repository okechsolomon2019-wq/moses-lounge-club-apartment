# Moses Lounge Club & Apartment

A responsive, installable website for Moses Lounge in Sukmamur, South Sudan. It is built with plain HTML, CSS, and JavaScript and can be published with GitHub Pages.

## Publish with GitHub Pages

1. Create a GitHub repository and add these project files to its `main` branch.
2. In the repository, open **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
3. The included workflow publishes the site whenever you push to `main`. Open the Pages URL shown in the workflow or Pages settings.

This workspace is not connected to a GitHub repository yet, so you will need to create or select a repository and push these files before the public website can be deployed.

## Prepare for Google Play

The Android package ID selected for Moses Lounge is `com.moseslounge.clubapartment`. A Play Store app has not been generated or submitted: the website must first have its permanent public HTTPS URL, and the owner must create a Google Play Console developer account.

1. Publish the website using GitHub Pages and confirm its permanent HTTPS URL.
2. Create and verify the owner's Play Console developer account. Keep account passwords, payment details, and signing keys private; never add them to this repository.
3. Build an Android Trusted Web Activity (TWA) for the published URL using the package ID above. The TWA must use the same final web origin as the published site.
4. Sign the Android App Bundle with the owner's release key. Add the matching SHA-256 signing-certificate fingerprint to `/.well-known/assetlinks.json` on that website origin so Android can verify the TWA.
5. Complete the Play Console app details, store listing, privacy policy and data-safety declarations, upload the signed bundle, and submit it for Google's review. Approval and publication are controlled by Google.

The TWA bundle and domain-verification file cannot be completed before the final website URL and release signing certificate exist. The website currently stores accounts and booking requests only in the visitor's browser; disclose this accurately in the store listing and Play Console declarations.

### Draft Play Store listing

These are draft texts to review and update after live bookings and account handling work end-to-end:

- **App name:** Moses Lounge Sukmamur
- **Short description:** Book rooms, shops, club packages and event spaces in Sukmamur, South Sudan.
- **Full description:** Discover Moses Lounge Club & Apartment in Sukmamur, South Sudan. Explore self-contained rooms, monthly shop rentals, the lounge, conference and party halls, and the club package. Check the published rates and prepare a booking request. Contact manager Mandel Peter by phone to confirm availability. **In this current demo, booking requests and account information stay in the browser on the visitor's device and are not sent to Moses Lounge.** Update this disclosure before the app is submitted if the service changes.
- **Privacy policy URL (after publishing):** `https://YOUR-GITHUB-PAGES-DOMAIN/YOUR-REPOSITORY/privacy.html`
- **Support contact:** Mandel Peter, +211 929 994 005 / +211 923 759 776

The listing should not promise confirmed online reservations or working Google sign-in until those features are connected to a secure service. Capture genuine screenshots from the final published app; do not present mockups as app functionality. Complete Play Console content rating, target audience, app access, ads, and data-safety declarations truthfully for the release build. Google's requirements can change; follow the current Play Console prompts.

## Install on a phone or computer

Open the published HTTPS website in Safari on iPhone and use **Share → Add to Home Screen**. In Chrome or Edge on a computer or Android phone, use the browser's **Install app** option. The website also keeps its main pages available offline after the first successful visit.

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
