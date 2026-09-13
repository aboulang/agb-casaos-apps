# Application intake

The following applications belong in this store after their known-working Compose definitions are supplied or exported from `testrig`:

- ComfyUI
- PeerTube
- Snapotter
- Scriberr

Do not create installable placeholders under `Apps/`. A folder is added only after its runtime configuration, persistent paths, ports, and required devices have been verified.

## Export an app managed by CasaOS

Replace `APP_ID` with the local CasaOS application ID:

```bash
sudo casaos-cli app-management show local APP_ID --yaml
```

Before committing an export, remove passwords, tokens, API keys, private hostnames, and other secrets.
