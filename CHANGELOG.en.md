# Changelog

[Italiano](CHANGELOG.md) · **English**

Download the latest version: <https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat>

## 2.7 — 2026-10-27

- **Mxntal desktop wallpaper** entry in Windows and interface: the M and the lettering on the aurora, drawn at the screen resolution; the previous wallpaper comes back on restore. AnyDesk among the installable apps.

## 2.6 — 2026-10-27

- Language choice at the first start, with flags: Italian, English, French, Spanish. Change it from the bottom-right button. Window, catalog and check-up are translated; the console stays in Italian.

## 2.9 — 2026-10-28

- Packs updated to the new catalog. Base: Telegram, Notepad++ and Visual C++ x86 (paired with x64) added. Gaming: Battle.net and Rockstar Games Launcher added.

## 2.8 — 2026-10-28

- Apps page: 106 programs in 10 categories (was 33 in 7), each with its official icon, and a search box. In the console the apps are picked by category.
- "Installed" is now decided by Windows' installed programs list (plus MSIX packages), with winget as a second check: Chrome, CrystalDiskInfo and Visual Studio Code no longer show as "to install" when they are there.

## 2.5 — 2026-10-27

- **What's new** window at the first start after an update: the changelog lines of the versions you skipped and the new Optimize entries (tagged "nuova"), with a button to open them. Also when you replace the file by hand.
- The engine uses `findstr` instead of `find`: with Git Bash or MSYS in PATH the selftest and the service, OneDrive and Explorer checks no longer fail.

## 2.4 — 2026-10-27

- Six new entries: manufacturer apps for devices off, End task from the taskbar, Edge without pop-ups and without MSN, WPBT, long paths

## 2.3 — 2026-10-26

- Update check at every start and, while the window is open, every hour: it used to be once a day.
- The new-version notice appears only once; "Aggiornamento X.Y" stays at the bottom with the Aggiorna (update) button.

## 2.2 — 2026-10-26

- **Controlla aggiornamenti** (check for updates) button at the bottom right: tells you whether you are up to date, what went wrong, or opens the release notes with **Aggiorna**.
- Two-column bottom bar: with little room, no more text under the buttons.

## 2.1 — 2026-10-26

- **Widgets OFF** blocked by Windows (UCPD driver): Mxntal explains it and points to the alternative Windows allows, instead of a bare error.
- Write errors show the reason given by reg.exe; after an error no phantom backup and no restart prompt.
- Pill-shaped progress bars; names and bars aligned in Overview and Optimize.

## 2.0 — 2026-10-26

- New name **Mxntal** and a graphical interface in the same single file: Overview with check-up, Optimize, Profiles, Apps, Cleanup, Time machine, Busted myths. The console menus stay (`/console`).
- Signed updates: the window checks the latest GitHub release and installs it with one click, only if the signature is valid.
- Domain-joined PCs: sensitive entries explain why and ask for confirmation; profiles and "apply all" skip them.
- File, backup folder, log and variables stay those of Mxntal.tweaks: old backups keep working.

## 1.8 — 2026-10-20

- Backups safe with special characters (`! % ^ "` and trailing backslash), which could corrupt the saved value before.
- Every write is read back and compared with the intended value; if it differs, the entry is marked as failed.
- New `/doctor` and `/verify`, log in `%LOCALAPPDATA%\MxntalTweaks`, backup integrity check and `.reg` export.
- Over 30 bugs fixed in menus, preview and PowerShell blocks; selftest, lint and menu driver extended.
