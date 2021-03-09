# Troubleshooting

## USB Connection

The camera should mount as an external drive when connected to a computer via USB. Sometimes, driver issues may cause the USB connection to fail, with or without an error message. It may also connect as a USB High-Speed \(480Mb/s\) device instead of a USB SuperSpeed \(5Gb/s\) device. Typical real-world file transfer rates when connected as a SuperSpeed device are 250-300MB/s \(2.00-2.40Gb/s\).

The following tips can help recover a valid USB SuperSpeed connection:

### General:

* Make sure the USB cable and the USB port are both rated for USB 3.x SuperSpeed. They should be marked "SS".
* Try removing and reconnecting the USB cable.
* Try rebooting the camera.
* Try a different order of operations: Sometimes powering on the camera with the USB cable already connected to the computer works better. In other cases, having the camera powered on first, then connecting the USB cable works better.
* Try a different USB port.
* Try a different USB cable.
* Try rebooting the computer.

### Windows 10:

* Open **Device Manager** and observe if any new devices are shown when the camera USB cable is connected. If one comes up, but it isn't an external drive, right-click the new device and select **Uninstall device**. Then, disconnect and reconnect the USB cable.
* Try the additional troubleshooting steps listed [here](https://support.microsoft.com/en-us/topic/usb-port-may-stop-working-after-you-remove-or-insert-a-usb-device-1eaf82a6-04b1-2604-f096-2345d9c215ef), including resetting the USB controllers \(Method 3\).

## HDMI Preview Quality

Due to hardware constraints, the camera only does a limited amount of decoding and image processing for the HDMI preview. As a result, the HDMI preview image quality is lower than the recorded image quality. When recording at 4K, the HDMI preview quality is closer to 1080p. When recording at 2K, the HDMI preview quality is closer to 480p.

This can make focusing in 2K mode with a shallow depth of field more challenging. If the scenario permits, you can set the focus point in 4K mode and then switch to 2K mode. Some additional focus assist tools are planned for future firmware updates.

