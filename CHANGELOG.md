# Release notes

## 1.1.1 — 6 October 2026

- Fixed loss of high-frequency detail when converting music and effects to the 48 kHz playback mix. The previous converter could make original 44.1 kHz effects sound dull or muffled.
- Improved conversion for both music decks, sound-effect pads and headphone preview while preserving pitch, duration and stereo channels.
- Added audio-fidelity checks for frequency balance, alias rejection and consistent cached/streaming playback.

Use **Check for updates** or download the new Windows x64 ZIP. Close the old app, extract the entire ZIP to a new folder, and run its **GenAssist DJ System Pro.exe**. Your existing library, effects and volume settings remain available; reimporting effects is unnecessary.

## 1.1.0 — 6 October 2026

- Added **Developer: GENESES C. ABARCAR** to the console, updates window and application metadata.
- Added **Check for updates**, connected to the official public GitHub releases. Reports newer versions, current version, unavailable releases and connection errors. Audio stays available while checking.
- Added a professional vinyl/G icon with a teal play accent, embedded in the executable, window and app header. Includes seven Windows icon sizes.
- Refined the console with a graphite theme, teal/blue deck accents, clearer transport states, consistent buttons, dark sliders and scrollbars, search hints and improved table spacing.
- Established separate private source and public release repositories.

Extract the Windows x64 ZIP and run **GenAssist DJ System Pro.exe** from the extracted folder. Close an existing copy before replacing files. Saved library data remains under `%LOCALAPPDATA%\GenAssist\DJSystemPro`.

The package is self-contained and unsigned. No DJ FX PRO sounds are included. Physical speaker/headphone separation still requires two playback devices; Jamendo requires the user's client ID.
