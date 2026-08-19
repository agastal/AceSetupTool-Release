# ACE Setup Tool

**English** | [Italiano](README.it.md) | [Español](README.es.md)

ACE Setup Tool is a Windows desktop application for managing, comparing and analysing
car setups in **Assetto Corsa EVO**. It reads and writes `.carsetup` files, imports
MoTeC telemetry and provides performance diagnostics.

> Official binary-distribution repository. Source code is not distributed.

## Download

Download the installer, portable build and checksums from the
[Releases](https://github.com/agastal/AceSetupTool-Release/releases) page.

- `AceSetupTool-<version>-setup.exe` — recommended installer;
- `AceSetupTool-<version>-portable.zip` — no-installation build;
- `AceSetupTool-<version>-setup-net.exe` — smaller installer for machines that already
  have .NET 10;
- `AceSetupTool-<version>-portable-net.zip` — the same build without installation;
- `SHA256SUMS.txt` — SHA-256 fingerprints for the release assets.

GitHub Releases is the only official distribution channel. Do not download executables
from mirrors or third-party links.

## Features

- read, edit and back up `.carsetup` files;
- compare setups and export CSV files;
- export the current setup values to a paginated PDF;
- import MoTeC telemetry into a local archive;
- compare an archived lap with an external MoTeC `.ld` file using animated trajectories;
- diagnose tyre pressures, temperatures, suspension, camber and ride height;
- display charts and track maps;
- Italian, English and Spanish interface;
- automatic Windows light/dark theme.

## Requirements

- Windows 10/11 x64;
- Assetto Corsa EVO;
- no separate runtime: .NET and Windows App SDK are included.

Installation is per-user and does not require administrator privileges. The portable
archive must be extracted in full: do not copy only the executable.

The `-net` assets are the same program without the bundled .NET runtime: 158 MB instead
of 235 once installed, and they need
[.NET 10 (x64)](https://dotnet.microsoft.com/download/dotnet/10.0) on the machine. The
Windows App SDK is included in those too, so .NET is the only prerequisite; the `-net`
installer checks for it and stops with a message instead of installing something that
would not start. If you are unsure, take the standard build.

To find out whether .NET 10 is there, open a terminal and run `dotnet --list-runtimes`:
if a `Microsoft.NETCore.App 10.x` line appears, the `-net` assets will work. If it does
not, or the command is not found, use the standard build. Windows does not ship .NET 10:
what comes preinstalled is .NET Framework, which is a different platform.

## Approved by Red Kongs

<p align="left">
  &nbsp;&nbsp;<img src="media/red-kongs.png" alt="Red Kongs Racing Team" width="245" hspace="16" vspace="6"/>
</p>

ACE Setup Tool is a tool **approved by Red Kongs**.

## Preview

### Setup and tyre parameters

<p align="center">
  <img src="media/01-setup-gomme.png" alt="Setup and tyre parameter editor" width="70%"/>
</p>

Select a car, track and saved setup, then edit pressure, camber and toe for every wheel
in real units. The header also shows the best lap, median and useful-lap count, while
the toolbar provides save, reload and CSV import/export commands.

### Side-by-side setup comparison

<p align="center">
  <img src="media/04-confronto.png" alt="Side-by-side comparison of two setups" width="70%"/>
</p>

Choose two configurations and inspect their parameters in one table, including units,
both values and highlighted deltas. A differences-only filter narrows the list, the
footer reports changed versus total parameters, and the result can be exported to CSV.

### Performance summary by setup

<p align="center">
  <img src="media/06-risultati-segnalazioni.png" alt="Performance metrics grouped by setup" width="70%"/>
</p>

Review each setup's best and median lap, lap count, hot pressure at all four tyres and
the share of the lap spent on the bump stops. This consolidated view makes pace,
consistency and key tyre and suspension indicators easy to compare.

### Throttle, brake and steering traces

<p align="center">
  <img src="media/07-risultati-grafici.png" alt="Throttle, brake and steering traces over lap distance" width="70%"/>
</p>

Plot throttle and brake percentages together with steering angle over lap distance.
Lap and comparison selectors make it easier to examine braking points, throttle
application and steering corrections at the same position on the circuit.

### Animated telemetry comparison

<p align="center">
  <img src="media/09-risultati-telemetria.png" alt="Animated comparison of an archived setup lap and external MoTeC telemetry" width="70%"/>
</p>

Overlay a lap stored for the selected setup with an external MoTeC `.ld` recording.
Playback keeps both car markers, speed, throttle and brake in sync; zoom, pan and fit
controls make trajectory and input differences easier to inspect.

### Race preparation and strategy calculation

<p align="center">
  <img src="media/08-preparazione.png" alt="Race preparation and strategy calculator" width="70%"/>
</p>

Enter race and qualifying duration, planned pit stops, pit-lane time loss, tank capacity
and fuel margin. The calculation uses the selected car and track to produce a strategy
summary based on the chosen setup and its median lap time.

## Data and privacy

Settings and the telemetry archive are stored locally:

| Data | Location |
|---|---|
| Settings | `%APPDATA%\AceSetupTool\` |
| Telemetry archive | `%LOCALAPPDATA%\AceSetupTool\` |

ACE Setup Tool does not implement user telemetry or remote transmission of setups or
driving data. Interactions with GitHub for downloads, Issues or other website features
are external to the application and subject to GitHub's terms. Do not post logs, setups
or telemetry containing information you want to keep private in a public Issue.

## Licence

ACE Setup Tool is **proprietary freeware**, distributed in binary form only. It may be
used free of charge under the [proprietary licence](LICENSE.txt) and the
[English EULA](EULA.en.txt). Courtesy translations are available in
[Italian](LICENSE.it.txt) and [Spanish](LICENSE.es.txt), with corresponding EULAs in
[Italian](EULA.it.txt) and [Spanish](EULA.es.txt). The English terms control to the
extent permitted by applicable law.

Licences and attributions for bundled components are available in
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and the
[`third-party`](third-party/) directory. Third-party licence texts remain in their
original language.

## Support

To report a problem, use [Issues](https://github.com/agastal/AceSetupTool-Release/issues) and
include the application version, Windows version and reproduction steps.

## Trademarks and affiliation

ACE Setup Tool is an independent, unofficial project. It is not affiliated with,
endorsed by or supported by Kunos Simulazioni or the publisher of Assetto Corsa EVO.
Product names and trademarks belong to their respective owners.

Copyright © 2026 Adriano Gastaldello. All rights reserved.
