# Fiesta Online PH — Auto-Patch Hosting (beta)

This public repository contains **update metadata and small test updates only**. Do not upload the full game client, passwords, SQL databases, private keys, account records, or any game assets you are not authorized to distribute.

## Architecture
- The game owner maintains an original client folder on their Windows desktop.
- An owner-side publisher creates a ZIP containing only changed files and uploads it as a GitHub Release asset.
- `patch-index.json` lists each release version, its download URL and full archive SHA-256.
- The Windows `FiestaPatcher.exe` reads this index, downloads pending patches, verifies archive and file SHA-256, and applies updates with rollback.
- The launcher checks automatically; players do not open GitHub or edit any files.

## Initial test
The first patch installs only `FiestaOnlinePH_Patch_Test.txt`, containing a harmless marker. Do **not** treat that file as a game asset.

## Important limits
- This is an early beta, not yet Windows-tested in the user's environment.
- Launcher EXE and updater EXE self-updates are intentionally blocked until a signed/bootstrap updater exists.
- A SHA in a mutable public manifest provides integrity but does **not** protect against a compromised maintainer account. Signing updates is a future hardening step.
- GitHub is a distribution service, not a substitute for legitimate rights to redistribute game files.

## Never upload
Full 5.25 GB Fiesta client, SQL .bak files, Pinggy tokens, passwords, secrets, private config, or unlicensed content.

