# Oceanova BioSync — Early Release

**[Download the BioSync 2.0.1 Windows trial](https://github.com/oceanovanz/biosync-downloads/releases/tag/v2.0.1)**

**Early Release — Community Trial.** Help test BioSync and shape future updates. Features, performance and AI accuracy are still being developed. This is an evaluation build, not a validated survey or species-identification instrument. Read the [trial notes and known limitations](EARLY-RELEASE.md) before installing.

Native Qt marine survey workstation with video, species review and online/offline GIS. This repository contains download information, release metadata and third-party notices. It does not contain BioSync's application source code, private observations or model weights.

## Windows 11 x64 — early community trial

Open the release page above and download **all four files into the same folder**:

1. `BioSync-2.0.1-windows-x64-setup.exe`
2. `BioSync-2.0.1-windows-x64-setup-1.bin`
3. `BioSync-2.0.1-windows-x64-setup-2.bin`
4. `BioSync-2.0.1-windows-x64-setup-3.bin`

Then run the setup `.exe`. Keep the three `.bin` files beside it; setup reads them automatically. Total download is approximately 3.1 GB. Leave **Create a desktop shortcut** selected for quick startup. GitHub's automatically generated **Source code** ZIP/TAR links contain only this downloads repository's documentation, not the application or installer.

The preview installer is unsigned. Windows may display a publisher warning; Oceanova publisher signing remains pending. Do not disable antivirus, SmartScreen or the firewall. SHA-256 receipts are included for integrity verification.

### Requirements

- Windows 11, x64; 16 GB RAM for the workstation, 32 GB recommended for full marine AI.
- A working Direct3D 11 graphics driver. The current marine AI engine requires a supported NVIDIA CUDA GPU; 16 GB VRAM is the validated development configuration.
- Current NVIDIA driver compatible with CUDA 12.8. Python, Qt and the AI runtime are included; a separate CUDA developer toolkit is not required.
- Reserve 40 GB for program/model setup, plus survey and recording storage.

### First start

Open **Tools → Installation / updates / local AI…** and download the pinned local AI models once (roughly 15 GB; allow 25 GiB free). Turn AI off before model setup. Afterwards select the marine engine and enable AI. Installed inference runs locally; online maps and requested update checks use the internet. Model suggestions remain unverified and require human review.

User data is stored in `%LOCALAPPDATA%\Oceanova\BioSync`. Updates and uninstall preserve that data folder. Back it up with BioSync closed before important updates. Existing development-folder data is not automatically moved; see [installation instructions](INSTALLATION.md).

## Linux

Linux binary downloads are **not available yet**. Ubuntu/Debian and portable builds require Linux validation. No application-source archive is distributed from this public repository.

## Updates and feedback

New public preview builds will appear under [Releases](https://github.com/oceanovanz/biosync-downloads/releases). The app checks for updates only when requested; there is no forced updater. Use this repository's Issues for reproducible software reports, without uploading sensitive locations, camera credentials or private survey footage.

## Source and third-party rights

BioSync application source is maintained privately. Public download availability does not grant a licence to copy or reuse Oceanova's application source. This notice does not restrict rights granted by third-party licences.

Qt/PySide6, FFmpeg, Python, PyTorch, CUDA components, pretrained models, maps and reference photographs retain their own licences and notices. Replaceable shared libraries and their notices are included in the installed `_internal` directory. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and the reference attribution ledgers. This repository does not claim exclusive ownership of those components.
