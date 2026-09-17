<div align="center">

# Plan

**Team capacity planning, on your desktop.**

[![Latest release](https://img.shields.io/github/v/release/XabAyca/plan-releases?label=latest&color=blue)](https://github.com/XabAyca/plan-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/XabAyca/plan-releases/total?color=brightgreen)](https://github.com/XabAyca/plan-releases/releases)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows-lightgrey)](#install)
[![License](https://img.shields.io/badge/license-proprietary-red)](#license)

*This repository hosts the public builds of the **Plan** desktop app.
The source code lives in a separate repository.*

</div>

---

## What is Plan?

Plan is a native desktop app to plan a team's capacity week by week: who is on
what topic, at what load, and when they're overbooked. It replaces the classic
"one giant spreadsheet" with a purpose-built UI: a planning grid with per-cell
gauges, a Gantt window per project, editors for people, holidays, absences and
assignments, and a diagnostics banner that flags every unplaceable assignment
in real time.

Plans can be stored **locally** or **shared through a GitHub repository** with
load-time conflict detection.

## Install

### macOS — via Homebrew (recommended)

```bash
brew tap XabAyca/plan
brew install --cask XabAyca/plan/plan
```

Upgrade later with:

```bash
brew update && brew upgrade --cask XabAyca/plan/plan
```

### macOS — manual `.dmg`

1. Grab the right build for your Mac from the [latest release](https://github.com/XabAyca/plan-releases/releases/latest):
   - Apple Silicon (M1/M2/M3/M4): `plan-<version>-aarch64-apple-darwin.dmg`
   - Intel: `plan-<version>-x86_64-apple-darwin.dmg`
2. Open the `.dmg` and drag **Plan.app** into `/Applications`.
3. **First launch only:** right-click Plan.app → **Ouvrir** → **Ouvrir**.
   Bundles are ad-hoc signed, so Gatekeeper needs one manual pass before
   remembering the app. Every subsequent launch is a normal double-click.

### Windows

1. Download `plan-<version>-x86_64-pc-windows-msvc.exe` from the [latest release](https://github.com/XabAyca/plan-releases/releases/latest).
2. Double-click to run. Windows SmartScreen may warn on first launch —
   click **More info** → **Run anyway**.

## Supported platforms

| OS      | Architectures       | Package        |
|---------|---------------------|----------------|
| macOS   | Apple Silicon, Intel | `.dmg` (Plan.app) |
| Windows | x86_64              | `.exe`         |

Linux is not built yet.

## Language

The UI ships in **French** and **English**. Switch via
*Paramètres → Personnel → Langue* — the choice is stored per user.

## Updating

- **Homebrew users**: `brew upgrade --cask plan`.
- **Manual users**: download the newest `.dmg` / `.exe` from
  [Releases](https://github.com/XabAyca/plan-releases/releases) and replace
  the existing app.

Every release page includes a changelog with the notable changes since the
previous version.

## Verifying a download (optional)

SHA-256 checksums are attached to every release. To verify:

```bash
# macOS
shasum -a 256 plan-<version>-aarch64-apple-darwin.dmg

# Windows (PowerShell)
Get-FileHash .\plan-<version>-x86_64-pc-windows-msvc.exe -Algorithm SHA256
```

Compare the output with the value published on the release page.

## Reporting a bug / requesting a feature

Open an issue right here on this repository:
[**plan-releases → Issues**](https://github.com/XabAyca/plan-releases/issues).
The source repository is private, so this is the public entry point for all
bug reports and feature requests.

Please include:

- your OS and version,
- the exact Plan version (visible in *Paramètres → À propos*),
- the steps to reproduce, and any relevant screenshot or log.


## License

Plan is proprietary software Xabi AYCAGUER. Redistribution of the binaries is
allowed for internal use only.

---

<div align="center">
Made with ❤️ in Rust.
</div>
