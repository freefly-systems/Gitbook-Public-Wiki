# Downloads

This page contains the latest versions, release notes, and previous versions of the [Wave Player \(Windows\)](downloads.md#wave-player-windows) software and the Wave [Camera Firmware](downloads.md#camera-firmware). Please note that both updates may be required to take advantage of the latest features. Updating the Wave Player alone does not automatically update the Camera Firmware.

## Wave Player \(Windows\)

{% file src="../../.gitbook/assets/waveplayer\_v1\_1\_0.zip" caption="Wave Player v1.1.0 \(Windows\)" %}

### Release Notes

#### v1.1.0 \(9 March, 2021\)

* Support for Camera FW v1.1.0.
* Color processing pipeline updated to better match the on-camera HDMI preview. Image adjustment order of operations and settings are now common to both, with settings values stored in clip metadata.
* New export options: Adjustable frame rate \(24/25/30fps\) and H.264.
* Support for 1920x1080 display resolution.
* GPU compatibility and performance improvements.
* Minor bugfixes.

#### v1.0.5 \(27 January, 2021\)

* Support for Camera FW v1.0.1 features and bugfixes.
* Removed redundant setup.exe. WavePlayerSetup.msi is the only program needed for install.

#### v1.0.4 \(8 January, 2021\)

* Improved GPU compatibility.
* Removed Calibration Mode checkbox, which was for internal use.

#### v1.0.3 \(21 December, 2020\)

* Improved GPU compatibility.

### Previous Versions

{% file src="../../.gitbook/assets/waveplayer\_v1\_0\_5.zip" caption="Wave Player v1.0.5 \(Windows\)" %}

{% file src="../../.gitbook/assets/waveplayer\_v1\_0\_4.zip" caption="Wave Player v1.0.4 \(Windows\)" %}

{% file src="../../.gitbook/assets/waveplayer\_v1\_0\_3.zip" caption="Wave Player v1.0.3 \(Windows\)" %}

{% file src="../../.gitbook/assets/waveplayer\_v1\_0\_1 \(2\).zip" caption="Wave Player v1.0.1 \(Windows\)" %}

## Camera Firmware

{% file src="../../.gitbook/assets/wavefirmware\_v1\_1\_0.zip" caption="Wave Firmware v1.1.0" %}

### Firmware Update Instructions

The camera firmware can be updated over USB using the following procedure:

1. Hold down the Scroll Wheel while pressing the Power Button to power up the camera in Firmware Update mode. Continue to hold down the Scroll Wheel until the Record LED flashes slowly.
2. Plug in the USB cable. The camera will appear as a USB drive. **This drive is separate from the one where clips are stored, so your footage won’t be visible but is safe and not affected by the firmware update.**
3. Drag the new firmware file \(WAVE.BIN\) into the fw folder.
4. Click the Scroll Wheel. The Record LED will begin to flash quickly as the firmware is updated.
5. Wait for the camera to automatically restart with the new firmware. This should take at most 30 seconds.

### Release Notes

#### v1.1.0 \(9 March, 2021\)

* Updates to compression and color pipeline.
* Improved out-of-the-camera color profile \(closer to Rec.709\). This does not affect recorded data, but provides a more color-accurate HDMI preview and matching starting point for the Wave Player image adjustments.
* Improved highlight handling, approximately 1/2-stop more dynamic range. This is done by allowing some sensor clipping and using the unclipped channels to recover highlight detail, aided by a smoother highlight desaturation curve. New image adjustments are available in the latest Wave Player to expose these settings.
* Improved match between HDMI preview and Wave Player image adjustment starting point. Image adjustment order of operations and settings are now common to both, with settings values stored in clip metadata.
* Added more scroll wheel filtering to prevent jumpy menu scrolling.
* Moved Shutter Line Artifact compensation to on-camera.
* Additional minor bug fixes and error handling.

#### **v1.0.1 \(27 January, 2021\)**

* Improved compensation for Shutter Line Artifact. This sensor artifact shows up as a dark row across the frame when one frame's exposure starts while the previous frame is still being read out, and is most severe in underexposed conditions. This firmware synchronizes exposure start to an exact row and, together with the latest Wave Player version, uses that information to better compensate for the artifact.
* Fixed a bug that could, in rare cases, cause image corruption after switching between 4K and 2K mode that would persist until the next power cycle. Momentary HDMI preview glitches during the 4K/2K mode switch are normal as the pipeline is reconfigured.

### Previous Versions

{% file src="../../.gitbook/assets/wavefirmware\_v1\_0\_1.zip" caption="Wave Firmware v1.0.1" %}

{% file src="../../.gitbook/assets/wavefirmware\_v1\_0\_0 \(1\).zip" caption="Wave Firmware v1.0.0" %}

## User Guide

The latest user guide is available [here](user-guide.md).

## 3D Model

[Shrinkwrap Model Link](https://a360.co/33uf94j) - Fusion 360 Web Viewer. \(Downloadable STEP file available here\)

