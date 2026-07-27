# Memomo Releases

This public repository is the official download and update-metadata home for Memomo for macOS.

- Apps are compiled locally, signed with a Developer ID Application certificate, submitted to Apple for notarization, and stapled before upload.
- GitHub does not build Memomo. GitHub Actions are disabled here.
- [Releases](https://github.com/SihoChoii/Memomo-Releases/releases) contains the direct-install ZIP and signed updater archive for each published version.
- `feeds/stable.json` and `feeds/beta.json` are the machine-readable update channels checked automatically when the Memomo interface loads.
- Beta releases are marked as GitHub prereleases and never replace the latest stable release.

Memomo’s application source is maintained privately and is not stored in this repository. GitHub’s automatically generated “Source code” archives for tags in this repository contain only this public distribution metadata, not the private app source.
