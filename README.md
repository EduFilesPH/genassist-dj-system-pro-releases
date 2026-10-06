# GenAssist DJ System Pro

**Developer: GENESES C. ABARCAR**

A professional Windows event audio console with two music decks, sound-effect banks, automatic playlist fades and independent headphone preview.

<img src="assets/app-icon.png" width="112" alt="GenAssist DJ System Pro icon">

![Console preview with sample data](assets/console.png)

## Download

Get the Windows x64 ZIP from the [latest official release](https://github.com/EduFilesPH/genassist-dj-system-pro-releases/releases/latest).

Version **1.4.0** adds local AI Stem pads for Vocal, Instruments, Bass, Kick and Hi-hat. It retains Hot Cues, Loop and Sampler pads, virtual music-library folders, the live-playback buzzing fix and in-app updates. Existing effects do not need to be imported again.

1. Extract the entire ZIP to a folder.
2. Open the extracted folder and double-click **GenAssist DJ System Pro.exe**. Keep the DLLs and runtime files alongside it.
3. Import MP3/WAV songs with **+ Files** or **Import folder**, load deck A or B, and play. Add your own effects to the sound-effect banks.

The download includes its .NET runtime. Application data is stored in `%LOCALAPPDATA%\GenAssist\DJSystemPro`.


## DJ controls and folders

**Set Cue** saves the current position; **CUE** pauses and returns there. Drag or scroll a jog wheel to seek; Shift gives finer movement. Choose **Hot Cues**, **Loop**, **Sampler**, or **Stems** above either deck's eight performance pads; each deck remembers its mode after restart.

- **Hot Cues:** click an empty pad 1–8 to save a position, then click again to jump and play. Shift-click or right-click clears it. Existing four-cue tracks keep their saved positions.
- **Loop:** **In/Out** marks a manual loop; **Exit** continues forward and **Reloop** recalls it. **½ Loop / 2× Loop** resize it, and **1s / 2s / 4s** loop that many seconds from the current position. Click the active length to exit. These loops use seconds and manual positions, without automatic beatmatching or beat quantization.
- **Sampler:** click to play/restart your existing bank sounds over music. Shift-click or right-click stops a sample. **‹ / ›** pages through eight sounds independently per deck. Bank selection, sound imports, labels and volume are in **Sound effects**. Both panels share the same sounds; sampler use and mode switching keep automatic music running.
- **Stems:** load an ordinary song, choose **Prepare**, and let the app separate and cache it locally while playback continues. Click Vocal, Instruments, Bass, Kick or Hi-hat to mute/unmute; Shift-click or right-click solos a part. Acapella, Instrumental and Reset provide common mixes. The first use automatically downloads the optional CPU engine (242 MB) and models (about 522 MB); no Python installation is needed and no music is uploaded. Preparation takes time and the five-part cache uses about 115 MB per minute. All-on playback uses the original samples. Separation quality varies by song; Instruments includes remaining percussion. See [the stem guide and model terms](STEMS.md), including the DrumSep weights' undocumented commercial-use license.

Choose **All music**, then **+ New folder** to create a folder. Select a folder first to create a subfolder. Ctrl-click or Shift-click songs, then drag them into a folder or use **Organize -> Add to folder**. Right-click a folder to rename or remove it. Parent folders include songs from their subfolders; **Unfiled** shows songs outside all folders. Removing a folder or its song references keeps songs in All music and keeps audio files in place. Folders and cue points are saved after closing the app.

## Updates

Use **Check for updates**, then **Update now** to download and verify a newer version while audio continues playing. When ready, choose **Restart and install**. The app saves your library, stops playback, installs and restarts with playback stopped. If the new app cannot confirm startup, the updater restores and restarts the previous version. Your library, imported effects and settings remain in local app data. Update checks send no account credentials or music-library data.

Versions before **1.1.2** need one manual download to gain this feature: close the old app, extract the entire new ZIP to a new folder and run its executable. In-app installation requires the complete Windows package in a writable folder, available staging space and no other copy running from that folder. Unsupported folders provide a manual-download fallback. Previous app folders and staged packages are retained for recovery and can be removed after confirming the new version works.

## Features

- Two independent decks with jog seeking, Cue/Set Cue and eight saved hot cues.
- Eight performance pads per deck with Hot Cues, manual/preset Loop, Sampler and local AI Stems modes.
- Sound-effect pads with overlapping playback, per-pad stop and shortcuts.
- Virtual music folders and subfolders with multi-song drag/drop and Organize menus. Audio files stay in their original locations.
- Music library, favorites, queue and saved playlists.
- Central mixer with vertical A/B channel faders, measured signal meters, master volume and crossfader.
- Automatic playlist playback with adjustable fades.
- Separate speaker and headphone output devices.
- Optional Jamendo discovery and licensed downloads using your own client ID.
- Clean dark console and native Windows app icon.
- In-app update downloads, verification, installation and restart with startup rollback.

This public repository contains release documentation and packaged downloads. Application source is maintained privately. Third-party notices and required third-party source/license files accompany the Windows download. Original DJ FX PRO audio is not redistributed.

The Windows binary is currently unsigned. Headphone isolation requires two separately addressable playback devices. Live Jamendo use requires your own client ID.
