# Release notes

## 2.1.0 — 7 October 2026

- Added Automix tempo matching. Each incoming song is synced to the playing one (tempo and beats, half/double time allowed) when both have a detected BPM and the change is at most 8%. After the crossfade it glides back to its own tempo at 0.4% per second, so tempos do not drift. **Match tempo** in the queue tab turns it off. Moving the deck's tempo fader during the glide hands control back to you.
- Added drag-to-load: drop library or queue songs, or MP3/WAV files from Windows, onto a deck or its waveform to load them paused. A playing deck refuses the drop.
- Sound-effect banks are now **groups**. Each deck's Sampler pads have their own group dropdown and keep their choice. Right-click a group dropdown to create, rename or remove groups, and right-click a sound to add it to or remove it from a group. Right-click menus now use the dark theme.

On 1.1.2 or later, use **Check for updates → Update now → Restart and install**. Library data, cue points, effects and settings are preserved. The Windows package remains unsigned.

## 2.0.0 — 7 October 2026

- Added a pro DJ layout. Stacked colored scrolling waveforms with beat lines, cue markers and loop region run across the top, with per-deck overview waveforms (click or drag to move through the song) and zoom.
- Added automatic BPM, beat grid and key detection, shown on the decks and as sortable BPM/Key library columns, plus **Analyze** for the library. Results are cached and refreshed when a file changes.
- Added tempo faders (±8/16/50%), **KEY** lock and jog-wheel pitch bend while playing. **SYNC** matches tempo, including half/double time, and lines up the beats.
- Added per-channel GAIN, HIGH/MID/LOW kill EQ and a low/high-pass FILTER. With every control centered, playback is sample-identical to 1.4.0.
- Added an **FX** pad page: Echo ½, Echo 1, Reverb, Flanger, Gate, Crush, Brake and FX Off. Echo and reverb tails ring out after stop.
- Loop pads become 2/4/8-beat auto loops snapped to the beat grid once the BPM is known.
- Added **REC** for 16-bit 48 kHz WAV recordings of the master mix. Auto playlist is now called **Automix**.

On 1.1.2 or later, use **Check for updates → Update now → Restart and install**. Library data, cue points, effects and settings are preserved. The Windows package remains unsigned.

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
