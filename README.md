# Dynamic Island for Windows

### A calm, always-on-top home for playback and quick system controls.

**Dynamic Island** brings the useful moments from Windows to a compact pill at the top of your screen. It is built for Windows x64 and published by **DODGE**.

> **[Download Dynamic Island for Windows x64](https://github.com/Dodge912/Dynamic-Island-for-Windows/releases/latest/download/Dynamic-Island-Setup-1.0.0-x64.exe)** · [View all releases](https://github.com/Dodge912/Dynamic-Island-for-Windows/releases)

## What it does

| Feature | What you get |
| --- | --- |
| **Now Playing** | Current Windows media-session title, artist, album art and playback state, with play/pause, previous/next, shuffle and track seeking. |
| **Windows volume** | A volume HUD synchronized with Windows master output volume, plus an in-card slider and mouse-wheel adjustment. |
| **Audio output** | View and switch the Windows default output device from the media card. |
| **System status** | Battery and charging status, microphone and camera activity, a microphone mute control, a camera privacy-settings shortcut, and a five-minute timer. |
| **Performance** | On-demand CPU and memory graphs with a short list of the busiest processes. Sampling runs while the performance panel is open. |
| **Clipboard** | A brief preview when text or an image is copied, with recent items available from the island. |
| **Drop to Hold** | Drop files onto the island to keep their paths handy temporarily. The files themselves are not moved. |
| **Dev Pulse** | Fresh Hacker News headlines alongside a locally selected developer motivation note. No AI account or API key is required. |

The island expands when you hover or interact, then returns to its compact state. Its motion uses spring-based transitions, and its transparent window passes clicks through outside the island.

## Install

1. Download `Dynamic-Island-Setup-1.0.0-x64.exe` from the latest release.
2. Run the installer and choose an install location.
3. On the finish screen, choose whether Dynamic Island should start when you sign in and whether to create a desktop shortcut.
4. Start playback in a Windows app that publishes a media session, then hover over or click the island to open the controls.

Only one copy runs at a time. If you start it again, the existing island is brought forward and the app explains that it is already running.

## Windows integration and privacy

Playback controls use Windows System Media Transport Controls. Volume and mute use the Windows audio endpoint. Battery, performance, clipboard, and privacy indicators read Windows system state; microphone mute and audio controls can change their corresponding Windows settings. Camera activity links to Windows privacy settings rather than attempting to disable the camera itself.

Dev Pulse fetches current headlines from Hacker News when opened. Its developer note is selected locally. The clipboard feature reads copied text or images to display its preview in the app. Do not copy sensitive content if you do not want it shown in that preview.

## Safety and publisher trust

The installer is attributed to **DODGE** and carries a timestamped signature made with a self-signed certificate for this build. Windows does **not** trust that certificate as a public publisher by default, so SmartScreen or Defender may still show a warning. A publisher name or signature is not a malware certification, and this build has not been independently security-audited. No Defender exclusions or security-setting changes are included.

If Windows warns you, review the file and its hash before deciding whether to run it. To check the SHA-256 value in PowerShell:

```powershell
certutil -hashfile Dynamic-Island-Setup-1.0.0-x64.exe SHA256
```

Compare the result with `SHA256SUMS.txt` attached to the same release. If you believe Microsoft Defender has made a false-positive detection, use [Microsoft Security Intelligence file submission](https://www.microsoft.com/en-us/wdsi/filesubmission). Do not add a Defender exclusion just to bypass a warning.

## Current release

- **Version:** 1.0.0
- **Platform:** Windows x64
- **Installer:** `Dynamic-Island-Setup-1.0.0-x64.exe`
- **Publisher:** DODGE
- **Repository contents:** Release information and the installer only; application source code is not published here.

### Known limits

- Media details and artwork depend on what the active Windows media session provides.
- Camera status is informational; the camera shortcut opens Windows privacy settings.
- Brightness controls and cloud-synced clipboard history are not part of this release.
- The live developer headlines require an internet connection.
