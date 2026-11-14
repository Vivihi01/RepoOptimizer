# REPO PC

**Optimize your PC. Maximize your FPS.**

REPO PC is a Windows utility designed to help optimize gaming performance, reduce unnecessary background activity, and inspect system performance.

<p align="center">
  <a href="https://github.com/Vivihi01/RepoOptimizer/releases/download/v0.3.0-preview.1/Repo.exe">
    <img src="https://img.shields.io/badge/DOWNLOAD-REPO%20FOR%20WINDOWS-5865F2?style=for-the-badge&logo=windows&logoColor=white" alt="Download REPO for Windows">
  </a>
  <br>
  <sub>Windows x64 · v0.3.0 Preview · 170 MB</sub>
</p>

**[View all releases](https://github.com/Vivihi01/RepoOptimizer/releases)** · **[Source code](https://github.com/Vivihi01/RepoOptimizer)**

> **Early access:** This is a pre-release build. Expect bugs and breaking changes. Only download if you understand that this is preview software.

## What's included

- Windows optimization and game-specific tweak catalog
- Hardware, GPU driver and live game monitoring tools
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

## Pre-release safety notes

- The MeshCentral agent executable is intentionally excluded from the public source snapshot. The Remote Support integration code/documentation is included; supply an appropriately configured agent through your own controlled release process and verify user-consent policies before distribution.
- Production verification keys have been replaced with setup placeholders. Insert only public verification keys; never commit private signing keys, API tokens or credentials.
- The updater still references AEOX production manifest/download endpoints. Test or disable the updater for local development before distributing custom builds.
- The source snapshot has not been compiled or tested in this environment. Build and validate it on Windows with .NET 9 before using it.

## Status

Early preview for source review and testing. Back up your system and inspect each system-level change before applying it.
