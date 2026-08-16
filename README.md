# North Star Cafe — Fire TV App

This Android/Fire TV wrapper opens the existing North Star Cafe digital-menu website directly in its clean TV mode:

`https://northstarcafemenu.com/?tv=1`

It does **not** redesign or replace the website. The existing online admin remains the source of content.

## Intended result

Fire TV Home → **North Star Cafe** → Open → full-screen digital menu, with no browser address bar, no INSTALL APP prompt, no page header/footer, and no scrolling.

## Build

1. Open this folder in Android Studio.
2. Let Gradle sync and install Android SDK 36 if Android Studio requests it.
3. Build → Build APK(s).
4. The debug APK will be generated under `app/build/outputs/apk/debug/`.

## Fire TV testing

Enable Developer Options / ADB debugging on the Fire TV, then install the APK with:

`adb install -r app-debug.apk`

The app declares `LEANBACK_LAUNCHER`, so it appears as a TV application after installation.

## Remote behavior

- D-pad/Select: passed to the web content when applicable.
- Menu key: refreshes the live menu.
- Back: navigates back only if the WebView has internal history; otherwise exits the app.

## Screen behavior

- Landscape locked.
- Immersive full screen.
- Screen stays awake while the app is open.
- HTTPS only.
- 16:9 / 1080p / 4K displays are supported by the underlying responsive TV view.

## Important

The website already contains a dedicated clean-TV mode activated by `?tv=1`. This wrapper deliberately relies on that existing behavior so changes made in the North Star admin continue to appear without rebuilding the Fire TV app.
