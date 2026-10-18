# BioSync 2.0.1 — Early Release / Community Trial

This trial lets early users explore the native desktop workstation and provide
feedback while development continues. It is not a stable production release or
a validated biological survey instrument.

## What this download contains

- The standard BioSync 2.0.1 Windows workstation.
- Local video/recording and supported camera/RTSP inputs.
- Marine AI model setup, unverified candidate review and a reference catalogue.
- GIS, user map imports and online/offline mapping tools.
- A desktop shortcut and manual update checks.

The separate **Fast Tracking Demo**, **Salmon Farm Demo** and **YouTube RTSP
Manager** are development tools and **are not included in this installer**.
The new tracking experiments have not been rolled into a public build.
Salmon demo labels are a presentation preset, not verified species recognition.

## Known trial limitations

- Detection, species suggestions and tracking are experimental. Fish can be
  missed, boxes can lag or disappear, and labels can be wrong. The number of
  boxes is not a validated organism count.
- Qwen interpretation can be slow or unavailable when there is no suitable
  candidate or insufficient model/GPU resources.
- Performance and camera/codec compatibility vary. Independent field accuracy
  and clean-machine coverage are still incomplete.
- Linux binaries, publisher code signing and automatic background updates are
  not available in this release.

Treat outputs as suggestions for human review. Do not rely on this build alone
for safety, biosecurity reporting, regulatory decisions or population estimates.

## Download and first start

Use the [Windows release page](https://github.com/oceanovanz/biosync-downloads/releases/tag/v2.0.1).
Save the setup EXE and all three BIN files into one folder, then run the EXE.
The installer download is approximately 3.1 GB. Keep Create a desktop shortcut
selected. The installer is unsigned, so Windows may display a publisher warning;
do not disable Windows security protections.

Full marine AI is a separate initial download of roughly 15 GB. Use Tools →
Installation / updates / local AI to set it up. Windows 11 x64, a supported NVIDIA
GPU with 16 GB VRAM, 32 GB RAM and 40 GB free storage are the recommended trial
configuration for the full engine. Actual device/driver compatibility still needs
testing. See [installation instructions](INSTALLATION.md).

Use sample data for initial trials, and back up your local profile before
installing later builds. Updates are installed manually; no unattended update
service is included.

## Send feedback

[Report an issue or suggest an improvement](https://github.com/oceanovanz/biosync-downloads/issues/new).
Include the version, Windows version, GPU, input type, steps to reproduce, and
what you expected versus what happened. A screenshot is useful where appropriate.
Do not upload private footage, sensitive survey locations, camera passwords or
other credentials. Reports on repeatable bugs are particularly helpful.

Application source remains private. Third-party licence and attribution rights
remain unchanged. Public availability is for evaluating the provided build.
