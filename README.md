# GenAssist DJ System Pro

**Developer: GENESES C. ABARCAR**

A professional Windows DJ console with two decks, colored scrolling waveforms, automatic BPM and key detection, tempo with key lock, SYNC, a three-band kill EQ and filter, FX pads, beat loops, mix recording, sound-effect groups, beatmatched Automix and independent headphone preview.

<img src="assets/app-icon.png" width="112" alt="GenAssist DJ System Pro icon">

![Console preview with sample data](assets/console.png)

## Download

Get the Windows x64 ZIP from the [latest official release](https://github.com/EduFilesPH/genassist-dj-system-pro-releases/releases/latest).

Version **2.1.0** adds Automix tempo matching, drag-to-load decks and sampler groups with a group dropdown per deck. Version 2.0 introduced the pro DJ console: waveforms, automatic BPM/key analysis, tempo with key lock, SYNC, a kill EQ and filter, FX pads, beat loops and mix recording. Hot Cues, local AI Stems, virtual folders and in-app updates are retained. Existing library data, cue points and effects are kept.

1. Extract the entire ZIP to a folder.
2. Open the extracted folder and double-click **GenAssist DJ System Pro.exe**. Keep the DLLs and runtime files alongside it.
3. Import MP3/WAV songs with **+ Files** or **Import folder**, load deck A or B, and play. Drag songs onto a deck to load them. Add your own effects to the sound-effect groups.

The download includes its .NET runtime. Application data is stored in `%LOCALAPPDATA%\GenAssist\DJSystemPro`.


## Pro DJ console

The layout follows professional DJ software. Stacked scrolling waveforms run across the top, deck A is on the left, the mixer is in the center and deck B is on the right. The library and sound effects sit below.

- **Waveforms:** colored by band (bass blue, mids teal, highs white), with beat lines, cue markers, the loop region and a red playhead. Each deck also has an overview of the whole song; click or drag it to move through the song. Scroll over the waveforms or use **+ / −** to zoom. The strip grows on taller screens.
- **Analysis:** loading a song detects its BPM, beat grid and key in the background, shown in Camelot and musical notation, for example **8A · Am**. **Analyze** in the library processes selected songs, or every song not yet analyzed. BPM and Key columns sort the library, and results are cached and redone if a file changes. Tempos are reported between 78 and 185 BPM, so half- or double-time music can read at the other octave; SYNC handles both. Detection is automatic and can be wrong on songs without a steady beat.
- **Tempo:** each tempo fader sits on the console's outer edge. Down is faster, as on DJ hardware; double-click to reset. **±8%** cycles through ±8, ±16 and ±50%. **KEY** (key lock, on by default) keeps the musical key when the tempo changes; turn it off for vinyl-style pitch.
- **SYNC:** matches tempo to the other deck (allowing half/double time) and lines up the beats when both decks play. Both SYNC buttons light while the tempos match.
- **Jog wheels:** while paused, drag to seek or scroll for one second. While playing, dragging bends the tempo to nudge beats into line.
- **Mixer:** each channel has GAIN (±12 dB), HIGH/MID/LOW EQ and a FILTER knob. Turning an EQ knob fully left kills that band; turning right boosts up to +6 dB. The filter is a low-pass to the left and a high-pass to the right. Level meters, channel faders, the crossfader and the MASTER knob complete the mixer. With every control centered, the audio is unchanged.
- **REC:** records the master output to a 16-bit 48 kHz WAV in `Music\GenAssist Recordings`. Right-click it to open or change the folder.
- **Automix** (formerly Auto playlist) plays the queue with crossfades. With **Match tempo** (queue tab, on by default), each incoming song is beatmatched to the playing one before the crossfade, then glides back to its own tempo at 0.4% per second. Matching needs detected BPM and is used for changes up to 8%; other songs simply crossfade.
- **Drag to load:** drag a song from the library or queue onto deck A or B, or onto its waveform (upper A, lower B), to load it paused. MP3/WAV files or folders dragged from Windows onto a deck are imported first. A playing deck refuses the drop.

## Deck pads and folders

**Set Cue** saves the current position; **CUE** pauses and returns there. Choose **Hot Cues**, **Loop**, **Sampler**, **Stems** or **FX** above either deck's eight performance pads; each deck remembers its mode after restart.

- **Hot Cues:** click an empty pad 1–8 to save a position, then click again to jump and play. Shift-click or right-click clears it. Existing four-cue tracks keep their saved positions.
- **Loop:** **In/Out** marks a manual loop; **Exit** continues forward and **Reloop** recalls it. **½ Loop / 2× Loop** resize it. Once the BPM is detected, the last three pads are **2 / 4 / 8-beat** auto loops that start on the nearest beat. Before analysis, they loop 1, 2 or 4 seconds. Click the active length to exit.
- **Sampler:** click to play/restart sounds from the group chosen in that deck's dropdown under the pads. Shift-click or right-click stops a sample. Each deck keeps its own group, for example deck A **Horns** and deck B **Drops**, and **‹ / ›** pages through eight sounds. Groups are categories of sounds: create one with **+ Group** or by right-clicking a group dropdown. Right-click a sound to add it to a group or remove it. Sounds stay in your library, and sampler use keeps automatic music running.
- **FX:** **Echo ½**, **Echo 1**, **Reverb**, **Flanger**, **Gate** and **Crush** follow the song's tempo and can be combined. Echo and reverb tails ring out after you switch them off, even after Stop. **Brake** slows the deck to a vinyl stop, and **FX Off** clears every deck effect.
- **Stems:** load an ordinary song, choose **Prepare**, and let the app separate and cache it locally while playback continues. Click Vocal, Instruments, Bass, Kick or Hi-hat to mute/unmute; Shift-click or right-click solos a part. Acapella, Instrumental and Reset provide common mixes. The first use automatically downloads the optional CPU engine (242 MB) and models (about 522 MB); no Python installation is needed and no music is uploaded. Preparation takes time and the five-part cache uses about 115 MB per minute. All-on playback uses the original samples. Separation quality varies by song; Instruments includes remaining percussion. See [the stem guide and model terms](STEMS.md), including the DrumSep weights' undocumented commercial-use license.

Choose **All music**, then **+ New folder** to create a folder. Select a folder first to create a subfolder. Ctrl-click or Shift-click songs, then drag them into a folder or use **Organize -> Add to folder**. Right-click a folder to rename or remove it. Parent folders include songs from their subfolders; **Unfiled** shows songs outside all folders. Removing a folder or its song references keeps songs in All music and keeps audio files in place. Folders and cue points are saved after closing the app.

## Updates

Use **Check for updates**, then **Update now** to download and verify a newer version while audio continues playing. When ready, choose **Restart and install**. The app saves your library, stops playback, installs and restarts with playback stopped. If the new app cannot confirm startup, the updater restores and restarts the previous version. Your library, imported effects and settings remain in local app data. Update checks send no account credentials or music-library data.

Versions before **1.1.2** need one manual download to gain this feature: close the old app, extract the entire new ZIP to a new folder and run its executable. In-app installation requires the complete Windows package in a writable folder, available staging space and no other copy running from that folder. Unsupported folders provide a manual-download fallback. Previous app folders and staged packages are retained for recovery and can be removed after confirming the new version works.

## Features

- Pro DJ layout with stacked scrolling waveforms, beat grids and per-deck overview waveforms.
- Automatic BPM, beat grid and key (Camelot) detection with sortable library columns.
- Tempo faders (±8/16/50%) with key lock, SYNC with beat alignment and jog-wheel pitch bend.
- Per-channel gain, HIGH/MID/LOW kill EQ, low/high-pass filter, level meters and crossfader.
- One-click WAV recording of the master mix.
- Two independent decks with jog seeking, Cue/Set Cue and eight saved hot cues.
- Eight performance pads per deck with Hot Cues, beat/manual Loop, Sampler, local AI Stems and FX modes.
- Sound-effect pads with overlapping playback, per-pad stop and shortcuts.
- Virtual music folders and subfolders with multi-song drag/drop and Organize menus. Audio files stay in their original locations.
- Music library, favorites, queue and saved playlists.
- Automix queue playback with adjustable crossfades and optional tempo matching.
- Drag-to-load decks and sampler groups with a group dropdown per deck.
- Separate speaker and headphone output devices.
- Optional Jamendo discovery and licensed downloads using your own client ID.
- Clean dark console and native Windows app icon.
- In-app update downloads, verification, installation and restart with startup rollback.

This public repository contains release documentation and packaged downloads. Application source is maintained privately. Third-party notices and required third-party source/license files accompany the Windows download. Original DJ FX PRO audio is not redistributed.

The Windows binary is currently unsigned. Microphone input, MIDI controllers, video and MP3 recording are not included. Headphone isolation requires two separately addressable playback devices. Live Jamendo use requires your own client ID.
