# GenAssist DJ System Pro

**Developer: GENESES C. ABARCAR**

A professional Windows event audio console with two music decks, sound-effect banks, automatic playlist fades and independent headphone preview.

<img src="assets/app-icon.png" width="112" alt="GenAssist DJ System Pro icon">

![Console preview with sample data](assets/console.png)

## Download

Get the Windows x64 ZIP from the [latest official release](https://github.com/EduFilesPH/genassist-dj-system-pro-releases/releases/latest).

Version **1.1.2** adds in-app downloads, installation and restart. It also includes the 1.1.1 audio-fidelity correction. Existing effects do not need to be imported again.

1. Extract the entire ZIP to a folder.
2. Open the extracted folder and double-click **GenAssist DJ System Pro.exe**. Keep the DLLs and runtime files alongside it.
3. Import MP3/WAV songs with **+ Files** or **+ Folder**, load deck A or B, and play. Add your own effects to the sound-effect banks.

The download includes its .NET runtime. Application data is stored in `%LOCALAPPDATA%\GenAssist\DJSystemPro`.

## Updates

Use **Check for updates**, then **Update now** to download and verify a newer version while audio continues playing. When ready, choose **Restart and install**. The app saves your library, stops playback, installs and restarts with playback stopped. If the new app cannot confirm startup, the updater restores and restarts the previous version. Your library, imported effects and settings remain in local app data. Update checks send no account credentials or music-library data.

Versions before **1.1.2** need one manual download to gain this feature: close the old app, extract the entire new ZIP to a new folder and run its executable. In-app installation requires the complete Windows package in a writable folder, available staging space and no other copy running from that folder. Unsupported folders provide a manual-download fallback. Previous app folders and staged packages are retained for recovery and can be removed after confirming the new version works.

## Features

- Two independent decks with seek, volume and crossfader controls.
- Sound-effect pads with overlapping playback, per-pad stop and shortcuts.
- Music library, favorites, queue and saved playlists.
- Automatic playlist playback with adjustable fades.
- Separate speaker and headphone output devices.
- Optional Jamendo discovery and licensed downloads using your own client ID.
- Clean dark console and native Windows app icon.
- In-app update downloads, verification, installation and restart with startup rollback.

This public repository contains release documentation and packaged downloads. Application source is maintained privately. Third-party notices and required third-party source/license files accompany the Windows download. Original DJ FX PRO audio is not redistributed.

The Windows binary is currently unsigned. Headphone isolation requires two separately addressable playback devices. Live Jamendo use requires your own client ID.
