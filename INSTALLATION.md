# BioSync early-release installation

**Early Release — Community Trial.** Read [what is included and the known limitations](EARLY-RELEASE.md). The separate development demo launchers are not included in 2.0.1.

## Downloads

Windows: download `BioSync-2.0.1-windows-x64-setup.exe` **and every accompanying `.bin` file into the same folder**, then run the setup executable. The CUDA runtime makes the package large; the installer reads its numbered data files automatically. Setup installs for the current user, creates a desktop icon by default and adds a Start menu entry. Python is included. Administrator access is not normally required.

Linux binary downloads require Linux build and hardware validation and are not available in this preview. No application-source archive is provided here. macOS and ARM releases are not available.

## Requirements

| Component | Requirement / recommendation |
| --- | --- |
| OS | Windows 11 x64; Ubuntu 24.04+ x86-64 release target |
| Workstation RAM | 16 GB; 32 GB recommended for full marine AI |
| Display | 1280×800 or higher recommended; native window minimum 1000×620 |
| Graphics | Direct3D 11 on Windows; working OpenGL/EGL driver on Linux |
| Marine AI | NVIDIA CUDA GPU supported by the bundled CUDA 12.8 PyTorch runtime; 16 GB VRAM recommended and the validated development configuration |
| NVIDIA driver | Current driver compatible with CUDA 12.8. The CUDA developer toolkit is not required. AMD/Intel GPUs can display video/maps but the current marine engine requires NVIDIA CUDA. |
| Storage | Reserve 40 GB for app, model downloads and setup working space; additional space for recordings, tiles and observations |
| Internet | Required for initial model download, optional online maps and requested update checks. Local media, installed AI and downloaded maps work offline. |
| Cameras | USB/UVC camera or supported capture device; RTSP/TCP streams supported. Actual device/codec compatibility still requires a trial. |

## First start and models

Open **Tools → Installation / updates / local AI…**. Select **Download / repair local AI models** once. Roughly 15 GB of pinned OWLv2, DINOv2, Qwen3-VL and BioCLIP 2.5 weights download from Hugging Face. Reserve at least 25 GiB free while downloading. Existing downloads resume on retry. Turn live AI off before setup. The runtime is included; no separate Python, pip or CUDA toolkit setup is required for an installed build.

Model download progress and errors are logged to `model-setup.log` in the data folder. Reference photos and pretrained models remain subject to their own licences. Model outputs remain unverified suggestions; installing weights does not establish species accuracy.

## Data and updates

Installed Windows data: `%LOCALAPPDATA%\Oceanova\BioSync`.

Installed Linux data: `${XDG_DATA_HOME:-~/.local/share}/oceanova/biosync`.

The app stores surveys, settings, labels, SQLite databases, offline maps and model weights there, outside program files. Installing over an existing version preserves these files. Uninstalling removes program files/shortcuts and leaves your data. Back up the complete data folder with BioSync closed before important updates. Export CSV/GeoJSON is also available for observations.

This development source folder still uses its existing `data/` directory. It is not automatically moved or overwritten by installing a release. To transfer it, close BioSync and copy the full source `data/` contents into the installed data directory before collecting new surveys there. Avoid merging two separately used SQLite databases.

**Check for updates** is manual. It reads Oceanova's public HTTPS release manifest, then offers the official download page. Close BioSync and run the new installer. There is no forced updater or remote model execution. Public preview releases are listed at https://github.com/oceanovanz/biosync-downloads/releases.

## Windows download protection and networking

Installers should be Authenticode-signed with the publisher's certificate and distributed over HTTPS with SHA-256 receipts. A development/unsigned build may trigger SmartScreen; signing does not guarantee immediate reputation. Do not disable Defender, SmartScreen or the firewall to install BioSync. Publisher signing requires an Oceanova-controlled certificate or signing service; none is embedded in this repository. [Microsoft's developer guidance](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation).

BioSync does not install an HTTP server or a public listening service. Normal HTTPS downloads use outbound TCP 443. RTSP/TCP connects to the camera's configured port (commonly 554, or 8554 for the user's local relay). ONVIF discovery uses UDP multicast 239.255.255.250:3702 and replies to the requesting socket; site policy can block it. Entering a camera address manually avoids relying on discovery. Explicit UDP stream inputs may need a narrowly scoped inbound exception for the configured port on a trusted survey network. The installer never creates a broad inbound rule.

Windows normally allows outbound traffic unless a blocking rule applies. Managed computers may need an administrator to allow the official download hosts and the survey camera network. [Windows Firewall rules](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/best-practices-configuring). Also enable camera access for desktop apps in Windows privacy settings; on Linux, check `/dev/video*` permissions and camera availability.
