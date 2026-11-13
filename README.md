# TUNE VVO

**Free vocal pitch correction by VVO Audio** — natural, transparent tuning that sounds like the studio standard, with a hard-tune mode when you want the effect.

**[⬇ Download the latest version](https://github.com/vvoaudio/tunevvo-releases/releases/latest)**

| | macOS Tahoe | macOS Universal | Windows |
|---|---|---|---|
| File | `TuneVVO-<version>-macOS.pkg` | `TuneVVO-<version>-macOS-Universal.pkg` | `TuneVVO-<version>-Windows-Setup.exe` |
| Needs | macOS 26 Tahoe or later | macOS 11 Big Sur or later | Windows 10 or later · 64-bit |
| Macs | Apple Silicon (M1 and later) or Intel | Apple Silicon (M1 and later) or Intel | — |
| Format | VST3 + Audio Unit (AU) | VST3 + Audio Unit (AU) | VST3 |
| Installs to | `/Library/Audio/Plug-Ins/VST3/` and `/Library/Audio/Plug-Ins/Components/` | same | `C:\Program Files\Common Files\VST3\` |

**Which Mac file?** On macOS 26 Tahoe either one works. On anything older (Big Sur 11, Monterey 12, Ventura 13, Sonoma 14, Sequoia 15) use the **Universal** file.
It sounds identical — same plug-in, built to run on older macOS. It is also in the [`macOS-Universal`](macOS-Universal/) folder of this page.

## Install on Mac
1. Download the `.pkg` (Universal if your Mac is older than macOS 26 Tahoe) from the [latest release](https://github.com/vvoaudio/tunevvo-releases/releases/latest) and double-click it.
2. macOS will say it can't verify the developer (TUNE VVO is free and not registered with Apple). Click **Done**, then open
   **System Settings → Privacy & Security**, scroll down and click **Open Anyway** next to the TuneVVO message. Confirm with your password.
3. Click through the installer (it asks for your administrator password).
4. Restart your DAW or rescan plug-ins, and load **TUNE VVO** from your VST3 or Audio Unit plug-ins (Logic and GarageBand use the Audio Unit).

## Install on Windows
1. Download the `.exe` from the [latest release](https://github.com/vvoaudio/tunevvo-releases/releases/latest) and run it.
2. If Windows shows **"Windows protected your PC"**, click **More info → Run anyway** (TUNE VVO is free and not code-signed).
3. Click through the installer (it asks for administrator permission).
4. Restart your DAW or rescan plug-ins, and load **TUNE VVO** from your VST3 plug-ins.

## Updating
Already have TUNE VVO (or its earlier name, VvoTune)? Quit your DAW, then run the new installer the same way. It replaces the old version
(including any older copy in your own plug-in folder), and keeps your presets, saved scales and projects:
sessions open with the same settings and the same sound.

### Update notice (from the version that includes it)
Once a day TUNE VVO asks GitHub which version is the latest (one request to `api.github.com`; nothing else is sent). If a newer one exists, an
**UPDATE AVAILABLE!** button appears at the top of the window. Click it: the installer for your system is downloaded, checked against the published
SHA-256 checksum and opened. Quit your DAW and finish the installer, as above. Nothing is installed without you.
To turn the check off, right-click the button and choose **Turn off update checks** (or create an empty file named `update-checks-off` in
`~/Library/Application Support/VvoTune/` on Mac, `%APPDATA%\VvoTune\` on Windows). Delete that file to turn it back on.

## Quick guide
- **Key / Scale** — choose the song's key and scale, or click the keyboard to switch notes on and off (add notes outside the scale, remove notes from it). **Save Scale** keeps your own note sets.
- **Retune Speed** — how fast notes are pulled to pitch. 0–20 ms: tight, hard-tune; 20–100 ms: natural; 100–400 ms: gentle, vibrato kept. The ring colour shows how hard it is working.
- **Strength** — how much correction is applied (0 % = untouched).
- **Hard Tune** — holds the note even through wide vibrato for a steadier, flatter robotic effect. Off = natural note changes.
- **Low Latency** — about 3 ms delay for recording while monitoring through the plug-in (normal mode: 15 ms, fully compensated by your DAW).
- **Presets** — **Save Preset** stores Retune, Strength, Hard Tune, Low Latency and the scale (not the key). **Default** is always available.
- **Settings (gear, top right)** — **Theme**: choose **Dark** (the original black rack faceplate) or **Light** (weathered silver). **Particle animation**: untick it to remove all particles from the glass and keep CPU use low; ticked, the particles move at your monitor's refresh rate, in step with the screen. Both choices are remembered.

## Uninstall
- **Mac:** delete `/Library/Audio/Plug-Ins/VST3/TuneVVO.vst3` and `/Library/Audio/Plug-Ins/Components/TuneVVO.component`.
- **Windows:** Settings → Apps → **TUNE VVO (VST3)** → Uninstall.

Presets and saved scales live in `~/Library/Application Support/VvoTune` (Mac) or `%APPDATA%\VvoTune` (Windows).

---
TUNE VVO is free for personal use and provided as is, without warranty. VST is a trademark of Steinberg Media Technologies GmbH.
Third-party licences: see [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
