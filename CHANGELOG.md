# Release notes

## 1.1.3 — 6 October 2026

- Fixed buzzing and distortion during live Windows playback, including a single deck. Previous audio samples were being left in the playback buffer and accumulated into later audio.
- Corrected buffer clearing for both decks, sound effects and headphone preview. Original audio files and saved volume settings are preserved.
- Added a regression check using the same byte-backed audio buffers as Windows playback. Verified the correction with real WASAPI loopback capture of both decks against direct playback.

On **1.1.2**, use **Check for updates → Update now → Restart and install**. Older versions require extracting the complete ZIP and running its executable. Existing effects do not need to be imported again. The Windows package remains unsigned.

## 1.1.2 — 6 October 2026

- Added **Update now** with download progress and cancellation. Downloads run while music continues playing.
- Added **Restart and install** to save the library, stop playback, install and restart inside the app. Playback stays stopped after restart.
- Added official GitHub SHA256 verification, a complete file inventory, executable-version checks and validation of archive paths and sizes.
- Added startup confirmation and automatic rollback/restart when the new version cannot finish starting. Previous app folders are retained for recovery; personal files in the app folder are preserved.
- Added manual-download fallback for unsupported folders/packages, plus Windows file-lock retries and checks for other running copies.

**Install this version manually once if you are using 1.1.1 or earlier.** Close the old app, extract the complete ZIP to a new folder and run its executable. Future supported releases can then update from inside the app. Library data and effects remain in local app data. The Windows package remains unsigned.

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
