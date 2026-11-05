# PRISM Releases

Public **downloads-only** repository for PRISM Windows beta.

This repository is **not** the PRISM source tree.
Source remains at [abiyevfahraddin-cyber/PRISM](https://github.com/abiyevfahraddin-cyber/PRISM).

## What you will find here

- Versioned NSIS installer assets (GitHub Releases) — **only after owner release authorization**
- Signed beta update channel metadata (`channel/beta/`)
- Public Ed25519 verification key fingerprint for the PRISM updater
- Install notes and Windows “unknown publisher” expectations

## What you will **not** find here

- PRISM source code
- Internal architecture / authority documents
- Private signing keys
- Tokens, user data, QA profiles, or secrets

## Windows unsigned warning

Current beta installers are **not** Authenticode-signed with a paid Windows publisher certificate.
Windows SmartScreen / Defender may warn about an unknown publisher. That warning is **expected** and is **not bypassed** by PRISM.

PRISM’s own updater additionally verifies:

1. Detached **Ed25519** signature of the release manifest
2. HTTPS allowlisted download origin
3. Exact installer byte length + SHA-256
4. Explicit user consent before running the installer

HTTPS + SHA-256 alone are **not** treated as authenticity of the manifest.

## Install (when a release asset exists)

1. Download the official `PRISM-Setup-*.exe` from this repository’s **Releases** page.
2. Read the Windows warning carefully.
3. Install only if you intended to download from this official repository.
4. Do not run installers from forwarded chat files or unknown mirrors.

## Beta update channel

- Channel id: `beta`
- Manifest path (GitHub Pages, when enabled):  
  `https://abiyevfahraddin-cyber.github.io/PRISM-RELEASES/channel/beta/latest.json`
- Product id: `prism-windows-nsis`

Until the first owner-authorized public installer is published, the channel file may be a **placeholder** and must not be treated as a production update feed.

## Verification key

See [`keys/README.md`](./keys/README.md).

## License / notices

PRISM product licensing is separate from open download availability.
Downloading does **not** automatically grant commercial rights.
Third-party notices for Chromium/Electron components ship inside the installer package.

## Status

`PUBLIC_REPO_INFRASTRUCTURE=YES`  
`FIRST_INSTALLER_PUBLISHED=NO` (requires separate owner release authorization)  
`OWNER_ACCEPTED=NO`
