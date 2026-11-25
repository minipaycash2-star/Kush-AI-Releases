# KushAI Releases

This repository hosts official KushAI release assets distributed through GitHub Releases. Release files are attached to a versioned GitHub Release; installers and signing material should not be committed to the repository.

Each application release is expected to include these three assets:

- `KushAI_Setup.exe` — the Windows installer.
- `KushAI_UpdateManifest.json` — the update metadata, including the installer SHA-256.
- `KushAI_UpdateManifest.sig` — the detached signature for the exact manifest bytes.

Before installing an update, KushAI verifies the manifest signature with its embedded public key and checks that the downloaded installer matches the SHA-256 in the verified manifest. If either verification fails, the installer is not run.

Do not commit private signing keys, DPAPI-protected key backups, or release binaries to this repository. Attach the three release assets to the corresponding GitHub Release instead.
