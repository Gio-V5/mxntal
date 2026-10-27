<p align="center"><img src="docs/brand/mxntal-logo-128.png" width="96" height="96" alt="Mxntal"></p>
<h1 align="center">Mxntal</h1>
<p align="center"><strong>Lavora nell'ombra. Tu giochi.</strong> · It works in the shadows. You play.</p>
<p align="center">
  <a href="https://github.com/Gio-V5/mxntal/releases/latest"><img src="https://img.shields.io/github/v/release/Gio-V5/mxntal?label=version&color=8A4FD8" alt="Latest version"></a>
  <a href="https://github.com/Gio-V5/mxntal/releases"><img src="https://img.shields.io/github/downloads/Gio-V5/mxntal/total?label=downloads&color=8A4FD8" alt="Downloads"></a>
</p>
<p align="center"><strong>English</strong> · <a href="README.it.md">Italiano</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a></p>

Mxntal tunes Windows 10 and 11 with no black boxes: every change has a written reason, a backup of the
previous value and a one-click restore. It is a single file, `MxntalTweaks.bat`, with a graphical
interface and, for those who prefer them, the classic console menus. Nothing to install. The interface is
in Italian.

![Mxntal's Optimize page](docs/screenshot-ottimizza.png)

## Download and run

1. Download the latest version: **[MxntalTweaks.bat](https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat)**
   (about 640 KB).
2. Double-click it: Windows asks for administrator rights and the window opens. If you refuse, Mxntal
   closes without changing anything.
3. On the first run Windows may warn that the publisher is unknown: that happens with every `.bat` file
   downloaded from the internet.

Requirements: Windows 10 or 11 with an administrator account; Windows PowerShell 5.1 (already in Windows);
for the Apps page, winget ("App Installer" from the Microsoft Store).

## What it does

- **Panoramica** (overview): a check-up with a score and the things to fix, each with the button that
  fixes it; CPU, memory, graphics card and disk in real time; the PC's spec sheet.
- **Ottimizza** (optimize): 30 entries in 7 categories (power and CPU; gaming and input; Windows and
  interface; startup, RAM and background; disk and services; internet and network; advanced). Every entry
  explains what it changes, the risky ones ask for confirmation; "apply the safe ones" and "restore
  category" do it all at once.
- **Profili**: quick profiles, Gaming and Work.
- **App**: 32 common programs installed with winget, from the makers' official packages.
- **Pulizia** (cleanup): junk files (temp, dumps, logs and, if you choose, the Recycle Bin), measured
  before removal; preinstalled apps (43 in the list), removed for the current user and restorable with one
  click; programs that start with Windows.
- **Backup**, the time machine: every saved value with its restore, Windows restore points, scheduled
  restart.
- **Miti** (busted myths): the famous tweaks Mxntal does not apply, and why.

## What it never touches

- Microsoft Store, Windows Update, Delivery Optimization, Xbox services, Xbox Game Bar and Game DVR
  recording.
- No placebo tweaks: Win32PrioritySeparation, NetworkThrottlingIndex, HPET and the like stay out; the
  Myths page explains why.
- Settings Windows protects with the UCPD driver (for example Widgets on some PCs): Mxntal does not work
  around it, it explains the block and points to the alternative Windows allows.
- On a domain-joined PC the DNS stays the company one, and sensitive entries (indexing, security
  protections, Defender exclusions, TCP) explain why and ask for confirmation.

## Backup and restore

- Before every change the original value goes to `%LOCALAPPDATA%\MxntalTweaks\Backup\originali`, one
  file per value, and it stays the pre-Mxntal value even if you apply an entry several times.
- Every write is read back: if the value is not the intended one, Mxntal says so and the entry is marked
  as failed.
- Restore from the window: Backup, one value at a time or all at once; Ottimizza, flip the switch off or
  "Ripristina categoria"; Pulizia, "Rimetti le app tolte". In the console: menu 9.
- The log in `%LOCALAPPDATA%\MxntalTweaks\MxntalTweaks.log` records date, action, value before and after,
  and the outcome.
- Only the file cleanup has no undo: that is why Mxntal measures first and asks for confirmation.

## Updates

At every start, and every hour while it stays open, the window checks for a new version (one 1 KB HTTPS
request, no data sent) and installs it with one click, only if it is signed. The **Controlla
aggiornamenti** button checks right away; "Non controllare più gli aggiornamenti" turns the automatic
check off. What changed in each version is in the [changelog](CHANGELOG.en.md).

## Classic console

| Command | What it does |
|---|---|
| `MxntalTweaks.bat /console` | the classic console menus, with administrator rights |
| `MxntalTweaks.bat /dryrun` | preview: shows what would change, touches nothing and asks for no rights |
| `MxntalTweaks.bat /doctor` | environment diagnostics: admin, Windows, PowerShell, tools, space, backups |
| `MxntalTweaks.bat /verify` | state of every entry and a check of the backups, read-only |
| `MxntalTweaks.bat /?` | list of modes |

From the window, the "Console classica" button at the bottom right opens the same menus. If the graphical
interface cannot start (for example PowerShell in constrained mode on a company PC), the console menus
open instead.

## Problems and ideas

Open an [issue](https://github.com/Gio-V5/mxntal/issues) with your Mxntal version and, if useful,
the log lines about the problem. Italian or English, both fine.
