# Seedboxes Software Releases

This repository hosts official releases and package repositories for Seedboxes software.

## Contents

- `sbagent/` - Binary releases for Seedbucket Remote Agent
  - `latest.json` - Latest version manifest with download URLs
  - `appcast.xml` - Sparkle appcast for macOS auto-updates
  - `VERSION/` - Version-specific releases with binaries and checksums

- `apt/` - Debian/Ubuntu APT repository
  - See [apt/README.md](apt/README.md) for installation instructions

## Download Latest Release

### Using latest.json

The `latest.json` file provides programmatic access to the latest release:

```bash
curl -s https://releases.seedboxes.cc/sbagent/latest.json | jq .
```

### Direct Downloads

Visit the latest version directory in `sbagent/` for direct binary downloads.

### APT Repository (Debian/Ubuntu)

Follow instructions in [apt/README.md](apt/README.md) to add the APT repository.

### macOS Auto-Updates

The macOS application includes Sparkle for automatic updates using:
https://releases.seedboxes.cc/sbagent/appcast.xml

## Verifying Downloads

Each version directory contains checksum files:
- `SHA256SUMS` - SHA-256 checksums
- `SHA1SUMS` - SHA-1 checksums
- `MD5SUMS` - MD5 checksums

Verify your download:

```bash
sha256sum -c SHA256SUMS
```

## Repository Structure

```
.
├── README.md
├── sbagent/
│   ├── latest.json
│   ├── appcast.xml
│   └── 1.0.0/
│       ├── sbagent-win-amd64.exe
│       ├── sbagent-darwin-universal.dmg
│       ├── sbagent-linux-amd64.deb
│       ├── sbagent-linux-arm64.deb
│       ├── sbagent-cli-linux-*
│       ├── SHA256SUMS
│       ├── SHA1SUMS
│       └── MD5SUMS
└── apt/
    ├── README.md
    ├── seedboxes-repo-key.gpg
    ├── conf/
    ├── dists/
    └── pool/
```

## Support

For issues or questions, please visit:
https://github.com/Rapiddot/seedboxes_releases/issues
