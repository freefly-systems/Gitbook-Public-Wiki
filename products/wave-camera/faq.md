# FAQ

## What resolutions and frame rates are supported?

The maximum frame rate in 4K \(17:9\) is **422fps** and in 2K \(17:9\) is **1461fps**. 2K uses subsampling, which preserves the crop factor of the Image Sensor but does not increase its light sensitivity. Other aspect ratios \(from 4:3 to 16:1\) are available with different maximum frame rates up to **9259fps** \(2048 x 128\). See [Maximum Frame Rates](maximum-frame-rates.md) for more details.

## What does "continuous recording" mean?

Wave records continuously to its internal SSD at all frame rates. This means it operates like a normal video camera: press the Record Button once to start recording and again to stop. The clip is immediately saved in SSD flash memory. There is no RAM buffer or trigger setup required. All recording is non-volatile \(power-down safe\).

## What types of lenses are supported?

Wave uses a passive, locking E-mount. **There is no electrical connection to the lens, so lenses with electronic focus or iris control are not supported.** Likewise, there is no autofocus. Wave is intended for use with manual lenses that cover a S35 sensor. Faster lenses \(with lower wide-open f-number or T-stop\) are preferable for shooting at high frame rates, where light is at a premium.

Because of its short flange focal distance, E-mount can be readily adapted to almost any other mount. The stock E-mount can be removed and other mount options may be added in the future. RED DSMC mounts are also supported with an optional spacer. See [Lens Recommendations](lens-recommendations.md) for a list of some good lens options for Wave.

## Does it have an on-board LCD?

No, an external HDMI monitor capable of receiving a 1080p30 signal is required to view the preview image and interact with camera menus. On-camera monitors typically also have useful tools such as histograms, waveforms, and focus assist. See [Monitor Recommendations](monitor-recommendations.md) for a list of some good monitor options for Wave.

Foregoing an on-board LCD allows the entire back surface of the camera to be used for heat sinking, which is important for high-speed capture. Embedded LCDs also tend to be lower resolution and/or brightness than readily available on-camera monitors.

## What are the key image sensor specs?

Wave uses a S35 color image sensor with 5.5μm pixels and a native resolution of 4096 x 3072 \(4:3\). The native ISO is 250 and the native dynamic range is 10-11 stops. It utilizes a global electronic shutter with shutter speeds ranging from 1s to 1s/66000.

This sensor is first and foremost about speed: it produces pixel data at up to 37.75Gb/s. It is not designed as an HDR sensor or a low-light sensor, although HDR modes that extend the dynamic range by 2-3 stops at lower frame rates may be added. Review the sample footage provided to make sure it will work for your application.

## What is the native recording format? Export format?

Clips are recorded internally in a native file format optimized for speed. This format is compressed Bayer RAW with a typical compression ratio of 5:1 to 6:1. These files can't \(yet\) be opened directly by other editing tools. WaveViewer is the PC software used to view native Wave clips, trim them, apply basic image adjustments, and export them to other formats. Export formats include Cineform, H.264, and PNG/JPEG sequences.

## Do I need a PC to work with Wave files?

For now, yes. The WaveViewer PC software used to view and export Wave clips runs on Windows 10. Other workflows, including WaveViewer Mac software and an Adobe Premiere Pro import plug-in, are planned.

## Is there an app for camera control?

Not at this time, but one is planned. \(The camera includes WiFi and Bluetooth.\)

## Can the SSD be replaced or upgraded?

Yes. The internal SSD is a standard M.2 NVMe SSD that can be replaced or upgraded. Only a small number of SSDs have been tested to meet the write speed requirements of Wave right now. But by using a standard interface, the camera can be upgraded as drives get bigger, faster, and cheaper. Details on the upgrade process will be posted at a later date.

## Does it record audio?

No. Since it's primarily a high-speed video camera, audio processing wasn't included.

