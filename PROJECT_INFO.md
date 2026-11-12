# Project information (maintainer notes)

## Source files received

- `Sims4_Pro.html` — source HTML supplied by the author. Copied to `index.html` for GitHub Pages and browser launch.
- `Sims4_Cheat.exe` — prebuilt Windows executable supplied by the author and copied unchanged to `release-assets/Sims4_Cheat.exe`.

## Inspection notes

- HTML is a single self-contained document with embedded CSS and JavaScript.
- The source has 103 cheat records across 11 categories.
- The `SKILLS` array contains 62 unique entries. Old visible labels said 47; these visible labels were updated in the public `index.html` copy.
- The `CAREERS` array contains 38 unique entries: 36 career paths and 2 school-grade entries.
- UI languages: Russian, Azerbaijani, Turkish and English.
- User preferences use localStorage/cookies; user-selected audio is stored through IndexedDB where supported.
- Voice search uses `SpeechRecognition` / `webkitSpeechRecognition` and depends on browser support and microphone permissions.
- The mini-window action calls `window.open()` with a compact window size. It does not enforce a native always-on-top flag.
- The executable is a PE32 x86 Windows GUI binary, UPX-packed. Embedded version strings include ProductName `Sims4_Cheat_Pro`, FileDescription `Created by Emin Mirkarimov`, CompanyName `@emin.mirkarimov` and LegalCopyright `Created by Emin Mirkarimov`.

## Reproducible build limitation

The author mentioned that the EXE was originally packaged from HTML and a BAT file, but the original packaging BAT was not present in the uploaded materials. The project therefore includes only the supplied prebuilt EXE and HTML source. `RUN_HTML.bat` is a newly written helper that launches the HTML in the default browser; it is not the original EXE packaging script.

The GitHub Actions workflow only attaches the already-built EXE to a published Release. It does not compile or modify that EXE.
