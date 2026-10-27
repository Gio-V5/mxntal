# Changelog

[Italiano](CHANGELOG.md) · **English**

Download the latest version: <https://github.com/tecnico-lgtm/mxntal/releases/latest/download/MxntalTweaks.bat>

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
