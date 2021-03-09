# FAQ

## What resolutions and frame rates are supported?

The maximum frame rate in 4K \(17:9\) is 422fps and in 2K \(17:9\) is 1461fps. 2K uses subsampling, which preserves the crop factor of the image sensor but does not increase its light sensitivity. Other aspect ratios \(from 4:3 to 16:1\) are available with different maximum frame rates up to 9259fps \(2048 x 128\). Continuous recording is possible at all frame rates from 1fps up to the maximum in increments of 1fps. See [Maximum Frame Rates](https://freefly.gitbook.io/freefly-public/products/wave-camera/maximum-frame-rates) for more details.

## What does "continuous recording" mean?

Wave records continuously to its internal SSD at all frame rates. This means it operates as a normal video camera: press the record button once to start recording and press it again to stop. The clip is immediately saved in SSD flash memory. There is no RAM buffer or trigger setup required, and the length of the clip is limited only by the SSD capacity. \(See [Specifications](https://freefly.gitbook.io/freefly-public/products/wave-camera/specifications) for more details.\) All recording is non-volatile and power-down safe.

## What types of lenses are supported?

Wave uses a locking mount compatible with E-mount lenses. **There is no electrical connection to the lens, so lenses with electronic focus or iris control are not supported.** Likewise, there is no autofocus. Wave is intended for use with manual lenses that cover a S35 sensor. Faster lenses \(with lower wide-open f-number or T-stop\) are preferable for shooting at high frame rates, where light is at a premium.

Because of its short flange focal distance, E-mount can be readily adapted to almost any other mount. See [Lens Recommendations](https://freefly.gitbook.io/freefly-public/products/wave-camera/lens-recommendations) for a list of some good lens options for Wave.

## Is there an on-board LCD?

No, an external monitor capable of receiving a 1080p30 HDMI signal is required to view the preview image and interact with camera menus. On-camera external monitors typically also have useful tools such as histograms, waveforms, and focus assist. See [Monitor Recommendations](monitor-recommendations.md) for a list of some good monitor options for Wave.

Foregoing an on-board LCD allows the entire back surface of the camera to be used for heat sinking, which is important for continuous high-speed capture. Embedded LCDs also tend to be lower resolution and/or brightness than readily-available on-camera monitors.

## Can an external HDMI recorder be used?

The HDMI output is limited to 1080p30 and has minimal image processing, so the use of an external HDMI recorder is limited. There is no RAW output over HDMI available.

## What are the key image sensor specs?

Wave uses a S35 color image sensor with 5.5μm pixels and a native resolution of 4096 x 3072 \(4:3\). The native ISO is 250 and the native dynamic range is 10-11 stops. It utilizes a global electronic shutter with shutter speeds ranging from 1s to \(1/66000\)s.

This sensor is first and foremost about speed: it produces pixel data at up to 37.75Gb/s. It is not designed as an HDR or a low-light sensor. Review the sample footage available to make sure it will work for your application.

## What is the native recording format? Export formats?

Clips are recorded internally in a lightly-compressed 10-bit RGB file format optimized for write speed. At present, these files can’t be opened directly by other editing tools. [Wave Player](https://freefly.gitbook.io/freefly-public/products/wave-camera/downloads) is the PC software used to view native Wave clips, trim them, apply basic image adjustments, and export them to other formats. Export formats include CineForm \(.MOV\), H.264 \(.MP4\) and PNG/JPEG sequences.

## Do I need a Windows computer to work with Wave files?

For now, yes. The [Wave Player](https://freefly.gitbook.io/freefly-public/products/wave-camera/downloads) PC software used to view and export Wave clips runs on Windows 10. \(Wave Player Mac software is in development.\) Refer to the following System Specifications for details on supported PCs.

| System Component | Minimum | Recommended |
| :--- | :--- | :--- |
| Operating System | Windows 10 | Windows 10 |
| CPU Cores | 4 | 8 |
| Memory | 8GB | 32GB |
| Graphics | 2GB VRAM | Dedicated, 8GB VRAM |
| DirectX Support | DX12 | DX12 |
| Display | 2560 x 1440 | 4K |
| USB | USB 3.x \(SS\) | USB 3.x \(SS\) |

Wave Player will not run on Parallels, as there is no support for DX12. It will run on a Boot Camp Windows installation.

See [Laptop Recommendations](https://freefly.gitbook.io/freefly-public/products/wave-camera/laptop-recommendations) for a list of some laptops that have been tested to work with [Wave Player](https://freefly.gitbook.io/freefly-public/products/wave-camera/downloads).

## Is there an app for Wave camera control?

Not at this time, but the camera hardware supports WiFi and Bluetooth, so one may be developed later.

## Can Wave run on external power? External batteries?

Yes, the DC Input accepts 12-26V from an external power supply \(included\) or battery, and draws a maximum of 24W to both run the camera and recharge the internal battery. This can be supplied by an external V-Lock battery for longer-duration mobile operation. Note that although the camera will operate at 12V, fully charging the internal battery requires at least 14V at the DC Input.

## Can the Wave SSD be replaced or upgraded?

Yes. The internal SSD is a standard M.2 NVMe SSD that can be replaced or upgraded. Only a small number of SSDs have been tested to meet the write speed requirements of Wave right now. But by using a standard interface, the camera can be upgraded as drives get bigger, faster, and cheaper. Details on the upgrade process will be posted at a later date.

## Does Wave record audio?

No. Since it’s primarily a high-speed video camera, audio processing wasn’t included.

