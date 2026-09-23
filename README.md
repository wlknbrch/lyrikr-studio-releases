# Lyrikr Studio Releases

This repository distributes official release assets for **Lyrikr Studio**, a local desktop workstation for designing lyric-driven music videos.

Lyrikr Studio brings media ingest, lyric alignment, a timeline editor, typography and motion design, local processing, and video export into one focused workflow. Start with a song or a video, shape its lyric timing and visual direction, then render the result locally.

> This is a release-assets repository. It does not contain the Lyrikr Studio source code.

## Current platform

The current experimental release supports **macOS on Apple Silicon** only (M-series Macs).

Support for Intel Macs, Windows, and Linux is planned for a later release.

## Install Lyrikr Studio

1. Open the latest release and download the `Lyrikr Studio_1.7.6_aarch64.dmg` asset.
2. Open the downloaded DMG.
3. Drag **Lyrikr Studio** to the **Applications** folder.
4. Open the app from Applications.

The first start may take a moment while macOS verifies the app.

### macOS security notice

Early experimental builds may not yet be notarized by Apple. If macOS warns that it cannot verify the developer, make sure you downloaded the file from this repository's official release assets. Then Control-click the app in Applications, choose **Open**, and confirm the dialog. Do not lower macOS's global security settings.

## Local runtime setup

Lyrikr Studio uses a managed local runtime for analysis and export. It contains the local processing tools required for audio extraction, vocal separation, transcription, alignment, and rendering.

On first launch, Lyrikr Studio checks whether that runtime is available. If it is missing, choose **Set Up Local Runtime** in the app. The app downloads and installs the matching runtime automatically; you do **not** need to unpack the runtime archive manually.

The managed runtime is installed here:

```text
~/Library/Application Support/Lyrikr Studio/runtime-managed/current
```

The runtime and processing stay on your Mac. Some optional AI model weights may download on demand when you explicitly choose a feature that needs them.

## Included assets

A macOS release can contain two related assets:

| Asset | Purpose |
| --- | --- |
| `Lyrikr Studio_1.7.6_aarch64.dmg` | The desktop application installer for Apple Silicon Macs. |
| `lyrikr-runtime-darwin-aarch64-v1.7.6.tar.gz` | The local processing runtime downloaded by the app during first-time setup. End users normally do not install this manually. |

If a SHA-256 checksum file is attached to a release, verify the downloaded asset before opening it:

```bash
shasum -a 256 "Lyrikr Studio_1.7.6_aarch64.dmg"
```

## Responsible use

Only use audio, video, lyrics, and visual material you have permission to process. Lyrikr Studio is experimental software; keep backups of important projects and exported work.
