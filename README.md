# REPO PC

**Optimize your PC. Maximize your FPS.**

REPO PC is a Windows utility for gaming optimization, system monitoring and performance diagnostics.

<p align="center">
  <a href="https://github.com/Vivihi01/RepoOptimizer/releases">
    <img src="https://img.shields.io/badge/DOWNLOAD-REPO%20FOR%20WINDOWS-5865F2?style=for-the-badge&logo=windows&logoColor=white" alt="Download REPO for Windows">
  </a>
  <br>
  <sub>Windows x64 · Latest release</sub>
</p>

**[Download the latest release](https://github.com/Vivihi01/RepoOptimizer/releases)** · **[Browse source](https://github.com/Vivihi01/RepoOptimizer)**

## What's new in the latest release

- **Updated color palette** across the application interface.
- **Live hardware monitoring:** CPU and GPU utilization, plus available CPU/GPU temperature readings.
- **Processes tab:** inspect running processes and their resource usage.
- **Startup apps:** view and manage applications configured to start with Windows.
- **Settings refinements:** adjustments to integrated-app settings.
- **Potato Graphics beta:** experimental low-graphics presets for supported games, including Fortnite and Retrac.
- **UI improvements:** smoother navigation and a more responsive interface, with interface lag addressed.
- **Major RAM optimization:** reduced typical memory usage from **600 MB+ to under 100 MB**.

Hardware temperature availability depends on the device, drivers and supported sensor interfaces. Potato Graphics is beta functionality; supported settings and results may vary by game and system.

## Other features

- Windows and game-specific optimization tweaks
- Hardware and GPU driver information
- Background process management and network diagnostics
- WPF user interface and 3D scan view
- Licensing components and automated tests

## Build from source (Windows)

Install the .NET 9 SDK, then run:

```powershell
dotnet test .\Repo.sln
dotnet publish .\src\Repo.App\Repo.App.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfExtract=true -o .\dist
```

WebView2 Runtime is required for the 3D scan view.

## Pre-release notes

This is experimental preview software. Expect bugs and breaking changes. Review every system-level change before applying it and keep a backup. Temperature readings may be unavailable on some hardware. Potato Graphics is a beta feature and should be tested carefully.

## Security and configuration

- Do not commit private signing keys, API tokens, credentials or customer/device data.
- Review the Remote Support consent and visibility configuration before distributing builds that include remote-support functionality.
- The updater and licensing components use REPO/AEOX service endpoints; custom builds may require maintainer-side configuration.
