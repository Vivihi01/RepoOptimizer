# REPO PC — Pre-release source

**Pre-release source snapshot** for REPO PC, a Windows desktop utility built with .NET 9 / WPF.

> This repository is a source-code preview, not a signed production build. Features that depend on REPO/AEOX services may not work from a community-built binary until the corresponding service configuration and public verification keys are supplied by the maintainer.

## What's included

- Windows optimization and game-specific tweak catalog
- Hardware, GPU driver and live game monitoring tools
- Background process management and network diagnostics
- WPF user interface, 3D scan view and app assets
- Licensing components and automated tests

## Build (Windows)

Install the .NET 9 SDK, then run:

```powershell
dotnet test .\\Repo.sln
dotnet publish .\\src\\Repo.App\\Repo.App.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfExtract=true -o .\\dist
```

WebView2 Runtime is required for the 3D scan view.

## Pre-release safety notes

- The MeshCentral agent executable is intentionally excluded from this public source snapshot. The Remote Support integration code/documentation is included; supply an appropriately configured agent through your own controlled release process and verify user-consent policies before distribution.
- Production verification keys have been replaced with setup placeholders. Insert only public verification keys; never commit private signing keys, API tokens or credentials.
- The updater still references AEOX production manifest/download endpoints. Test or disable the updater for local development before distributing custom builds.
- This snapshot has not been compiled or tested in this environment. Build and validate it on Windows with .NET 9 before using it.

## Status

Early preview for source review and testing. Expect bugs and breaking changes. Back up your system and inspect each system-level change before applying it.
