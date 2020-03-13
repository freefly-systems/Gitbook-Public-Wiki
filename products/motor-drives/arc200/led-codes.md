# LED Codes

"Slow" flashing = 1hz, "fast" flashing = 4hz

Solid Blue: In bootloader mode, unplug USB cable to bypass \(or power cycle if a manual indefinite bootload cycle was initiated\). If you drive remains solid-blue after power on **without** a USB cable connected, the drive's firmware somehow went corrupt. Try loading the latest firmware, if it still fails, contact Freefly support to report the issue.

Slow Flashing Blue: Drive's EEPROM could not be loaded. This usually indicates some corruption. Try using the Erase Flash button in the GUI's Configuration tab to reset the memory chip.

Fast Flashing Blue: Loss of signal, out of range \(CAN, PWM\), or safety state awaiting neutral throttle position before starting after re-configuration \(PWM\). If this is reporting a loss-of-expected-signal, then this state persists for 2 seconds minimum for any trigger, or permanently if loss is more than 0.5 second. This indicates an unreliable communication between the drive and whatever is commanding it.

**Solid Green: Normal operating mode, no persistence**

Slow Flashing Green: under voltage in range of potential foldback or so far under voltage that the drive has completely disconnected phase outputs.

Fast Flashing Green: over voltage in range of potential foldback or so far over voltage that the drive has completely disconnected phase outputs.

Solid Red: Overheat foldback

Slow Flashing Red: Self-test failed at boot time. This usually indicates your drive suffered internal damage. The only other way to make this happen is trying to power the drive from a DC voltage outside the absolute max capabilities called out in the drive specs.

Fast Flashing Red: --unused--

Rapid White Flicker: The internal memory chips are being erased after receiving a wipe command from the user. This state should automatically clear in a few seconds when the erase operation is complete.

