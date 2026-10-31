<p align="center">
  <a href="README.md">한국어</a> · <a href="README.en.md">English (US)</a> · <b>English (UK)</b> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.fr.md">Français</a>
</p>

<p align="center">
  <img src="docs/icon.png" width="128" alt="Audio Mixer">
</p>

<h1 align="center">Audio Mixer</h1>

<p align="center">
  macOS menu bar audio mixer · Per-app volume · Equaliser · AutoEQ<br>
  <a href="https://github.com/jayusop/Audio-Mixer/releases/latest"><b>⬇ Download Latest</b></a> ·
  <a href="https://jayusop.github.io/Audio-Mixer/?lang=en-GB">Website</a>
</p>

<p align="center">
  <img alt="macOS 14.2+" src="https://img.shields.io/badge/macOS-14.2%2B-8f7dff">
  <img alt="Apple Silicon / Intel" src="https://img.shields.io/badge/Apple%20Silicon%20%2F%20Intel-supported-ff6fb6">
  <img alt="Free for personal & business use" src="https://img.shields.io/badge/license-freeware-3fb950">
  <img alt="Release" src="https://img.shields.io/github/v/release/jayusop/Audio-Mixer?color=5fe1f2">
</p>

---

A macOS app that lives in the menu bar and gives you **per-app volume**, **input/output device volume**, a **graphic/parametric equaliser**, and **AutoEQ headphone correction profiles**. No virtual audio driver required.

> Requirements: macOS 14.2 or later (Apple Silicon / Intel)<br>
> 🌐 The app's language follows your macOS system language: Korean, English (US/UK), Chinese (Simplified), Japanese, French. Other languages are shown in English.

## Installation

1. Download `AudioMixer.app.zip` from [Releases](https://github.com/jayusop/Audio-Mixer/releases/latest), unzip it, and move `AudioMixer.app` into your **Applications** folder.
2. The first time you open it, macOS shows a security warning (this personally distributed app isn't notarized by Apple). Don't click **Move to Bin** — close it with **Done** (**Cancel** on macOS 14), then click **Open Anyway** near the bottom of **System Settings › Privacy & Security**. Or, in Terminal:
   ```bash
   xattr -dr com.apple.quarantine /Applications/AudioMixer.app
   ```
3. A fader icon appears in the menu bar. The first time it processes audio it asks for **‘System Audio Recording’** permission → **Allow**. (If you missed it, turn it on in System Settings › Privacy & Security › Screen & System Audio Recording.)

> If it asks for permission again after an update, remove the old Audio Mixer entry from the permission list and allow it again.

## Features

| Area | Features |
|---|---|
| Mixer | Output/input device selection, hardware volume & mute, software volume for devices without hardware volume (e.g. HDMI) |
| Per-app volume | Auto-detects playing apps, 0–100% (optionally 200%), mute, level meters, remembers per-app settings, exclude from processing |
| Equaliser | 10-band graphic EQ (±12 dB), up to 32 parametric filters (PK/LSC/HSC/LP/HP/NO), frequency response curve, drag editing |
| AutoEQ | Search and apply from the AutoEQ database (~8,800 headphones/earphones) online (internet connection required), import/export ParametricEQ.txt |
| Presets | 17 built-in + user presets (save/overwrite/delete), **automatic preset switching per output device** |
| Sound protection | Auto preamp (attenuates by the max boost), peak limiter, hard-clip protection, L/R balance |
| Other | Launch at login, global processing on/off switch, Korean · English (US/UK) · Chinese (Simplified) · Japanese · French UI |

## Peace of mind

- **Never records**: audio is only processed in real time — never saved or sent anywhere.
- **Quit and your sound is unchanged**: if Audio Mixer quits (even unexpectedly), every app's sound instantly returns to normal.
- **Self-healing**: reconnects on its own after output device changes or sleep/wake.
- **No interference**: apps that output directly to another audio device (e.g. a DAW using an audio interface) are left alone.

## Notes / Limitations

- If you deny permission, per-app volume and EQ won't work (sound still plays normally); only device volume control is available.
- Right after an app starts playback there may be a very brief moment of unprocessed sound.

## Licence

Audio Mixer is freeware — **completely free for individuals and businesses**. No fee, no registration, no licence key.

- Use it at home or at work — companies, organisations, schools, commercial use (any number of Macs).
- Share unmodified copies free of charge, together with the licence.
- **The only thing not allowed is reverse engineering** — no decompiling, disassembling, or modifying/patching the binaries (except where the law says this can't be restricted).
- Provided ‘as is’, without warranty of any kind. No personal data is collected.

Full text: [LICENSE](LICENSE)

## Credits & Contact

- EQ profile data: [AutoEq](https://github.com/jaakkopasanen/AutoEq) (jaakkopasanen)
- Bug reports: [Issues](https://github.com/jayusop/Audio-Mixer/issues) · email jayusop@gmail.com
