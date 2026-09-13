# AGB CasaOS Apps

A custom CasaOS application store for AGB homelab systems.

The source tree is compatible with the zip-based third-party store mechanism used by CasaOS 0.4.4 on `testrig`. It also includes current store identity metadata so the same app definitions can be migrated to the newer v2 build format later.

## Add to CasaOS 0.4.4

Register the main-branch archive as an app-store source:

```bash
sudo casaos-cli app-management register app-store \
  https://github.com/aboulang/agb-casaos-apps/archive/refs/heads/main.zip
```

The source should then appear in the CasaOS App Store.

## Available applications

- **LiveKit Test Server** — LiveKit v1.13.5 in LAN-only development mode using host networking.
- **Whisper WebUI** — Local NVIDIA GPU-accelerated transcription and diarization on port 7860.

## Planned applications

- ComfyUI
- PeerTube
- Snapotter
- Scriberr

Their working Compose definitions will be added when recovered from `testrig` or supplied from the earlier installation work.

## Repository layout

Each installable application lives at `Apps/<AppName>/docker-compose.yml` and includes CasaOS metadata in its top-level `x-casaos` block.

Do not commit passwords, API keys, access tokens, private hostnames, databases, generated output, downloaded models, or application data.
