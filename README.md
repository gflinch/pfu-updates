# PFU Updates

Public update-only channel for Photo Field Unit.

This repository intentionally contains only update metadata and distributable APK packages. PFU source code, signing keys, credentials, and private development data remain outside this repository.

## Feed

PFU reads `latest.json` to discover the newest approved build.

The device requires:
- matching application ID
- `approved: true`
- a higher Android `versionCode` before downloading
- an HTTPS APK URL
- a 64-character SHA-256 checksum

PFU verifies the downloaded APK against the published SHA-256 before handing it to Android's package installer. Android then enforces the APK signing identity during installation.
