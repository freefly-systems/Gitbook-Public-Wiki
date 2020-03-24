# Troubleshooting

## I get Compass Inconsistency Errors when arming!

Troubleshooting steps:

* Make sure the sensor rotations are set correctly
  * In the Alta QGC parameters screen, search for "CAL\_MAG0\_ROT." In AltaX, this parameter should be set to "No Rotation" when the GPS is installed in the front, or "YAW\_180" when the GPS is installed in the rear
  * In the Alta QGC parameters screen, search for "SENS\_BOARD\_ROT." In AltaX, this parameter should always be set to "ROTATION\_YAW\_180"
* Perform compass calibration away from steel structures
  * Proximity to steel structures \(such as rebar in buildings or manhole covers on roads\) can sometimes interfere with compass calibration. As such, we suggest you perform compass calibration outdoors, away from buildings and any underground steel structures.

## Survey-in takes a long time to complete or does not complete

Cause: The Base Station GPS probably does not have good GPS lock

Fix: Move the GPS to a location with more open sky. Ensure that GPS is mounted on a stable platform, and that GPS is not moved after initial installation.

## Base Station GPS does not show up in Alta Ground Station

Cause: GPS serial connection was not recognized

Troubleshooting steps

* Make sure no other software is open that might be using the GPS com port
* In Windows, check device manager to see if GPS serial port appears.
  * If it does not appear, check USB cable
* Reboot computer

## Base Station safety LED is solid red

Cause: The GPS module has entered bootloader mode. This happens when the safety button is pressed while plugging the GPS module into the computer.

Fix: Unplug and re-plug the GPS module, taking care that the safety button is not pressed while plugging in.

## I accidentally changed the GPS settings!

By default, PX4 and Alta Ground Control only write configuration settings to the GPS's volatile RAM. This means that all setting are reset to their default settings when the module is re-powered.

If you have made permanent changes to the GPS by writing to its flash memory and the module no longer responds, you will have to reset its settings via USB.

To reset the GPS to its factory settings, you will have to download U-Center from U-Blox, using the following link: [https://www.u-blox.com/en/product/u-center](https://www.u-blox.com/en/product/u-center). Once you've installed U-Center, you can load the default Freefly GPS parameters found in the "Configuring" page of this Wiki.

## My aircraft GPS module does a cold restart on every boot

The GPS module has a supercap onboard to provide backup power, which allows you to perform a warm-restart, resulting in super-quick lock when re-powering the boards. However, this supercap only provides power for a limited time, typically less than one day. So, if the module has been disconnected for long enough, it will perform a cold boot, taking ~30s to acquire a lock.

Due to the need to perform survey-in, the base station GPS is commanded to perform a cold start every time you connect it to Alta Ground Control.

## My base station is in the wrong location in the Ground Control map

Cause: The base station was moved without restarting survey-in

Fix: Make sure you're using Alta QGC 1.3 or above. Stock QGC does not always restart RTK survey-in. To restart survey in in Alta QGC \(1.3 and above!\), use the RTK "Restart" button shown in the "[Using RTK Modules](rtk-quick-start.md#base-station-notes)" section.

## My aircraft is in the wrong location in the Ground Control map

Cause: Refer to the "[Base station in the wrong location"](rtk-troubleshooting.md#my-base-station-is-in-the-wrong-location-in-the-ground-control-map) section above.



