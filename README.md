<div align="center">

# 💎 The Sims 4 Cheat Studio PRO

### A multilingual cheat reference, search tool and command generator for The Sims 4

**Created by Emin Mirkarimov**

[![Windows](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows)](#download)
[![Languages](https://img.shields.io/badge/Languages-RU%20%7C%20AZ%20%7C%20TR%20%7C%20EN-2ea44f?style=for-the-badge)](#languages)
[![Release](https://img.shields.io/badge/Download-Latest%20Release-2ecc71?style=for-the-badge&logo=github)](https://github.com/eminmirkarimov/Sims4-Cheat-Studio-PRO/releases/latest)
[![License](https://img.shields.io/badge/Code-Copyright%20Reserved-red?style=for-the-badge)](COPYRIGHT.txt)

**[⬇ Download for Windows](https://github.com/eminmirkarimov/Sims4-Cheat-Studio-PRO/releases/latest) · [Русская инструкция](README_RU.md) · [Report a bug](https://github.com/eminmirkarimov/Sims4-Cheat-Studio-PRO/issues)**

</div>

---

## ✨ Overview

**The Sims 4 Cheat Studio PRO** is a fan-made companion application that helps players find, understand, generate and copy cheat commands for The Sims 4. It combines a searchable cheat encyclopedia with interactive generators for skills, careers, relationships and household funds.

The project is built around a self-contained HTML interface and is also distributed as a Windows executable (`Sims4_Cheat.exe`). The application prepares commands for the player to copy into the in-game cheat console. **It does not inject code into the game, modify save files, patch game files or bypass anti-cheat systems.**

## ⬇ Download

### Windows application

1. Open **[GitHub Releases](https://github.com/eminmirkarimov/Sims4-Cheat-Studio-PRO/releases/latest)**.
2. Download `Sims4_Cheat.exe` from the **Assets** section.
3. Run the file on Windows.

> The EXE in the first public release is the prebuilt file supplied by the author. The workflow in this repository attaches that file to a GitHub Release; it does not compile or rebuild the executable.

### Run the HTML version

Download `index.html` and open it in a modern browser, or run `RUN_HTML.bat` from the project folder. The browser edition is useful for inspecting the source and running the companion interface without the EXE.

## 🚀 Features

| Area | What it includes |
|---|---|
| Cheat encyclopedia | **103 cheat cards** across **11 categories**, with descriptions in four languages |
| Skill generator | **62 skill entries**, selectable levels and automatic command generation |
| Career / school generator | **36 career paths + 2 school-grade entries**, with promote, add, demote and remove actions |
| Relationship generator | Save Sim names, select two Sims and generate relationship commands with a slider from −100 to +100 |
| Household funds | Set a value from **0 to 9,999,999 §** and copy the generated `Money` command; quick presets included |
| Search and filters | Search cheat names, descriptions and entries; filter by category |
| Voice search | Optional browser speech recognition where supported and where microphone permission is granted |
| Languages | Russian, Azerbaijani, Turkish and English (RU / AZ / TR / EN) |
| Themes | Dark and light interface themes |
| Sound | UI sound effects, a “Sul Sul!” greeting and optional custom background audio |
| Personalization | Sim-name list, selected language, theme and other settings are stored locally by the browser |
| Mini-window | Opens a separate compact browser window; actual always-on-top behavior depends on the browser/window manager |
| Help bubbles | Contextual tooltips with Sims-style thought bubbles |

### Cheat categories in the included HTML

- ⚙️ Basics
- 💰 Money
- 🏠 Build mode
- ⚡ Needs
- 🎓 Skills
- 💼 Careers
- ❤️ Relationships
- 🌟 Traits
- 🧛 Occult
- 👻 Deaths & Ghosts
- 🌦️ Weather & World

## 🎮 How to use

1. Start The Sims 4 and load a household.
2. Open Cheat Studio PRO.
3. Find a command using search, category filters or the generator panels.
4. Click **Copy** on the required command.
5. Return to the game and press `Ctrl + Shift + C` to open the cheat console.
6. For cheats that require it, enter `testingcheats true` first.
7. Paste the copied command into the console and press Enter.

Some commands depend on the relevant game pack, installed content, active Sim, selected lot or current game version. Read the description before using a command.

## 🌍 Languages

The interface, category names, descriptions and help text include:

- 🇷🇺 Russian
- 🇦🇿 Azerbaijani
- 🇹🇷 Turkish
- 🇬🇧 English

Use the language selector in the top-right area of the application.

## 🔊 Custom audio and browser permissions

The app lets users select their own MP3 files for the “Sul Sul!” greeting and background music. Selected audio is stored in the browser's IndexedDB storage; general preferences use local browser storage. **Audio tracks are not included in this repository.** Only use audio you own or are allowed to use.

Voice search uses the browser's Web Speech API. It depends on browser support, microphone permission and the speech-recognition service available to the browser; it should not be described as guaranteed offline functionality. Browsers may also block automatic audio playback until the user interacts with the page.

## 🧩 Project files

```text
Sims4-Cheat-Studio-PRO/
├── index.html                         # Main HTML application and source
├── RUN_HTML.bat                       # Opens the HTML edition in the default browser
├── README.md                          # Main GitHub page (English)
├── README_RU.md                       # Russian user guide
├── GITHUB_SETUP_RU.md                 # Step-by-step publishing guide
├── RELEASE_NOTES_v1.0.0.md            # First release notes
├── CHANGELOG.md                       # Version history
├── COPYRIGHT.txt                      # Copyright notice / usage terms
├── DISCLAIMER.md                      # EA / Maxis independence disclaimer
├── PROJECT_INFO.md                    # Notes about the supplied EXE and source files
├── .gitignore
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml
│   │   └── feature_request.yml
│   └── workflows/
│       └── attach-release-exe.yml      # Adds the EXE to a published release
└── release-assets/
    └── Sims4_Cheat.exe                 # Prebuilt Windows executable for Releases
```

## 🛠️ Technical notes

- The browser edition is a self-contained HTML document with embedded CSS and JavaScript.
- Preferences are stored with browser storage; user-selected audio is stored in IndexedDB where available.
- Voice recognition is provided by the browser and is not guaranteed to work in every browser or in a local `file://` session.
- The supplied executable is a **PE32 x86 Windows GUI application** and is UPX-packed. Its version resource identifies the product as `Sims4_Cheat_Pro` and lists Emin Mirkarimov as its creator. It has not been rebuilt from the HTML as part of this repository package.
- The original packaging BAT file was not included in the supplied attachments. `RUN_HTML.bat` in this repository is a new helper that opens the HTML source; it is **not** the original EXE packer.

## 🧪 Status and feedback

This is the author's first public release package. If a command does not work, include the exact command, your game version, installed packs and a short description of the situation in a [Bug Report](https://github.com/eminmirkarimov/Sims4-Cheat-Studio-PRO/issues/new?template=bug_report.yml). Do not include save files or personal account information.

## 🗺️ Roadmap

- Review and verify cheat commands against game updates.
- Add filters for base game and expansion/game packs.
- Expand command explanations and troubleshooting notes.
- Improve keyboard navigation and accessibility.
- Add versioned change notes for cheat database updates.

## ⚖️ Disclaimer

This is an independent fan-made companion project. It is **not affiliated with, endorsed by or sponsored by Electronic Arts Inc. or Maxis**. The Sims and The Sims 4 are trademarks of their respective owners. See [DISCLAIMER.md](DISCLAIMER.md) and [COPYRIGHT.txt](COPYRIGHT.txt).

---

<div align="center">

**Created and maintained by Emin Mirkarimov**  
Instagram: [@emin.mirkarimov](https://www.instagram.com/emin.mirkarimov)

*Made for players who want their favorite commands one click away. Sul Sul! 💎*

</div>
