# Memomo for macOS

Memomo records microphone audio and optional computer audio, then transcribes and labels speakers locally on your Mac. Recording works without a speech model.

## Download and install

Visit [Releases](https://github.com/SihoChoii/Memomo-Releases/releases) and choose a published version. Prereleases are betas; use the latest stable release when one is available. If no releases are listed, public downloads are not available yet.

1. Download the `Memomo-<version>-macos-arm64.zip` asset. GitHub's automatically generated “Source code” archives do not contain the app.
2. Open the ZIP and drag `Memomo.app` into Applications.
3. Open Memomo from Applications and follow onboarding. Choose microphone access when you want to record; computer-audio capture is optional and requires Screen Recording access in macOS System Settings.

Published apps are signed with Developer ID, notarized by Apple, and stapled before upload. Do not disable Gatekeeper or remove quarantine to bypass an installation problem. Report the version and the macOS error through [Issues](https://github.com/SihoChoii/Memomo-Releases/issues).

## Requirements and limits

- Apple Silicon Mac; the app requires macOS 14 or newer. Intel and universal downloads are not offered. Compatibility testing for the first beta is still in progress.
- Recording does not require an internet connection or downloaded speech models. In Settings, you can choose to download a local transcription or speaker model before analysis.
- Reviewed model payloads are approximately 77 MB for Tiny transcription, 627 MB for the larger transcription model, and 11 MB for the speaker model. Allow additional space for downloads, model compilation, recordings, and exports. Processing also needs memory beyond the model file size.
- Recordings warn at 55 minutes and save/stop at 60 minutes. Transcription accepts up to 60 minutes; speaker analysis and combined analysis support up to 30 minutes. A longer combined request preserves transcription and reports the speaker-analysis limit. Inputs over 2 GiB are rejected.
- Force-quit, power loss, or stalled storage can interrupt saving. Keep backups of important recordings.

## Privacy and model setup

Recordings, transcripts, and speaker processing stay on your Mac. Memomo does not upload this content and includes no analytics, advertising, accounts, or cloud sync. Optional speaker memory stores names and voice embeddings locally; it can be cleared in Settings.

Network access is used for model downloads you request and for signed update checks/downloads. The main interface checks its build's update feed at startup; Settings also allows an explicit Stable or Beta check. Model hosts and GitHub can see normal request metadata such as your IP address. Downloading and installing an update require user action.

Built-in model preparation validates approved content. If an upstream model changes, setup may fail until a reviewed update is available. A failed setup does not prevent recording without analysis. Read the privacy notice and third-party notices included in the app for details.

## Updates and support

Use the app's update controls to install a newer signed version. Beta versions use the Beta feed; a stable publication moves both feeds to that stable version. Each published version has a higher numeric app version than the previous one.

[Report a bug or request help](https://github.com/SihoChoii/Memomo-Releases/issues). Include your Memomo version, macOS version, Mac chip, steps to reproduce, and the visible error. Do not post private recordings, transcripts, speaker names, or unredacted diagnostic files in public issues.

## Distribution files

Each published release contains the direct-install ZIP, its SHA-256 checksum, a signed updater archive and signature, and a redacted public attestation. The updater archive is for the app's updater; use the ZIP for manual installation.

Apps are compiled and verified locally. GitHub Actions are disabled here. The app source remains private; this repository contains only public download instructions and the `feeds/stable.json` and `feeds/beta.json` update metadata as they are published. Beta releases are GitHub prereleases and never replace GitHub's latest stable release.
