# Powering On and Throttle Safety

## Powering On <a id="PoweringOnandThrottleSafety-PoweringOn"></a>

When powering on the drive, if the USB cable is connected to the drive and a computer, the drive will enter bootloader mode indicated by a solid blue LED. This mode will exit within 10-15 seconds if no firmware update command is received and enter normal operating software. If powering with the USB cable disconnected, the drive will immediately bypass the bootloader and enter normal operating software.

After first power up, you will need to connect to the GUI using the supplied USB cable. The drive needs to be configured for your motor and application before it can operate. See the [ARC GUI](../../arc-gui/) section for information on this software.

## Throttle Disconnect Safety <a id="PoweringOnandThrottleSafety-ThrottleDisconnectSafety"></a>

The Arc200 handles a disconnected or broken throttle input in the following ways as a safety measure:

* PWM: If no PWM edge is detected in the timeout period of 50ms, the drive will command 0A if in torque mode, or 0RPM if in speed mode \(keep in mind in speed mode, going to 0RPM may involve high torques and a rapid change in motion!\).
* Analog: If an analog cable is disconnected, there is an internal pull-down resistor that will make the drive think the throttle is set at 0. **Make sure this is a safe state! This could present hazards if the drive would start accelerating in either direction for this throttle command.**
* GUI/QX API: If no QX packet is received in a 1-second period \(any QX packet, does not need to be a command packet\), the drive assumes the user has disconnected and commands 0A if in torque mode, or 0RPM if in speed mode.

After configuring your drive, you should test out the throttle disconnect safety! Get the motor spinning then manually unplug the throttle and make sure you are satisfied with what happens from a safety standpoint.

