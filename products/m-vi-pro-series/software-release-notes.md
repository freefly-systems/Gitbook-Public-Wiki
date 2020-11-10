# Software Release Notes

## Software Versions

\#protip​ - ​Verify all Freefly products are up to date by referencing the chart below to make sure there are no compatibility issues.

For instance, v2.0 GCU is not fully compatible with v1.5 MIMIC. So, if you plan to upgrade to v2.0 software bundle, make sure all your devices are updated to the versions specified for that bundle.

|  | 2.0 Beta | Stable |
| :--- | :--- | :--- |
| MōVI Pro    GCU | 2.0.16 | 1.5.2 |
|                      TSU | 2.0.1 | 1.5.2 |
|                      ESC | 1.1.0 | 1.0.2 |
| MōVI XL     GCU | 2.0.16 | 1.5.2 |
|                     TSU | 2.0.1 | 1.5.2 |
|                     ESC | 1.0.4 | 1.0.4 |
| MōVI Carbon GCU   | 2.0.16 | 1.6.4 |
|                     TSU I/O | 2.0.1/1.0.0 | 1.6.5/1.1.0 |
|                     ESC | 1.0.2 | 1.0.2 |
| MIMIC | 2.0.3 | 1.5.1 |
| MōVI Controller | 4.2.0 | 4.2.0 |
| MōVI Pro App   iOS | 2.0.2 | 1.5.x |
|                     Android | 2.0.4 | 1.5.x |



## Firmware Updates

To Update 

* Get the MōVI Pro App Beta App at [freeflysystems.com/beta](www.freeflysystems.com/beta)
* Connect to your MōVI Pro/XL/Carbon or MIMIC through the MōVI Pro iOS or Android App.
* Navigate to Monitor&gt;Updates, and check if you have the latest firmware.

 Notes

* MōVI Controller update is through [its own process](https://freeflysystems.com/support/movi-controller-support).
* MōVI subcomponent versions \(gcu, tsu, esc\) can be found on MōVI screen under Monitor&gt;Details&gt;Versions



\*\*\*\*

## **V2.0.2 RELEASE NOTES**

November 2020

v2.0.2 Software Bundle comes with new MōVI Pro/XL/Carbon firmware v2.0.16 and updated iOS/Android apps to enable features below:

* **Improvement**: Stabilization performance is improved under severe vibration conditions
* **Improvement**: Stabilization performance is improved for cases where there is a small amount of acceleration \(ex: dolly push on a slider\)
* **Improvement**: Default settings start with "user" preset. This way if user doesn't modify the preset selection, MōVI would behave exactly the same as pre-blackjack firmware
* **Improvement**: Default roll and tilt mode in 360 should be free and not snap.
  * Default for 360 off: Tilt locked, roll locked
  * Default for 360 on: Tilt free, roll free \(every time 360 roll is toggled on\)
* **Improvement**: Majestic Screen App UI relayout and include new settings introduced with Blackjack
* **Improvement**: Added smooth lock feature back to the timelapse mode to allow manually positioning MōVI by hand
* **Improvement**: Dual rocker to control pan and tilt independently for setting up timelapse
* **Improvement**: Updated all information texts inside the apps
* **Bugfix**: Removed features from the iOS app that were previously removed from the firmware
  * Target mode
  * Max Roll Angle
  * Output Master Filter
  * Shutter type
  * Shaky cam
* **Bugfix**: Compass declination is fixed.
* **Bugfix**: In the previous build of the iOS app, opening the expert settings screen would result in pan-for-roll coupling symptoms if running firmware v2.0.10 or below.
* **Bugfix**: Carbon was not resetting biases on boot, which could cause roll to be off a few degrees after boot. Additionally, GCU firmware v2.0.16 includes other improvements to eliminate potential roll issues for Carbon.
* **Bugfix**: On FW v2.0.11 and later, filter settings, such as drift assist mode wasn’t persisting on reboot
* **New**: New reset attitude button on iOS App and Movi Controller that will reset the sensors on the Movi Carbon to allow users to mitigate any attitude corruption in the field.





## **V2.0.1 RELEASE NOTES**

April 2019

* This release is an app only update \( iOS v2.0.1 and Android v2.0.3\)
  * This is a bugfix for “roll goes off when panning” symptom.
  * Root cause was loading a configuration file from the app to MōVI.
  * If you are experiencing this symptom, you should “reset robot settings”. There shouldn’t be any further problems using this app.

\*\*\*\*

## **V2.0.0 RELEASE NOTES**

December 2018

* **This the major release for Movi Pro/Carbon/XL called Blackjack! Read more about it** [**here**](https://freefly.gitbook.io/freefly-public/products/m-vi-pro-series/blackjack/whats-new)**.**

\*\*\*\*



## **V1.6 RELEASE NOTES**

**GCU - v1.6.4**

* New Feature: Support for MōVI Carbon.
* Internal
* New Feature: Support for external gyros + accelerometers on MōVI Carbon.
* New Feature: Added bias tracking startup ramp for external IMU’s that have warm up periods.
* Improvement: Updated UI to show when an external gyro + accelerometer is connected on MōVI XL and MōVI Carbon.
* Bugfix: The bias tracker no longer tracks Pan rotations using the accelerometer.

**TSU** 

* v1.6.5
  * Bugfix: Fixes an issue where FIZ position measurements wrap around and can give incorrect readings past their limits. This fix will prevent gimbal from having an incorrect zoom rate scale at zoom limits.
* v1.6.4
  * New Feature: Support for MōVI Carbon.
  * New Feature: Added zoom rate scaling feature which slows down camera movement the farther the lens is zoomed in. 
  * New Feature: FIZ Autocal on startup for MoVI Carbon.

**MōVI Controller**

* v3.6.0
  * New Feature: Zoom Rate Scaling UI so users can adjust the Zoom Rate 
  * New Feature: Default the lens profile on MōVI Carbon to Fujinon XK 20-120mm.
* v3.7.2
  * New feature: [Movi Wheels](https://store.freeflysystems.com/products/movi-wheels) support & TX Config screen updates

**iOS / Android Apps - v1.6.x**

* New Feature: Support for MōVI Carbon.

**Known Issues**

* Timelapse Controls Disappear on Movi Controller
  * Issue: Preview/Start Timelapse options disappear on controller; leaving only the cancel option.
  * Workaround: Setting up timelapses still works through the app.





## **V1.5 RELEASE NOTES**

**GCU v1.5.1**

* New Feature: FOG \(Fiber Optic Gyro\) support for MōVI XL

**TSU** 

* **v1.5.2**
  * Bugfix: MōVI Pro/XL compatibility issues with new version of RED firmware is fixed. Previously, upgrading RED firmware from v6 to v7 have introduced issues such as slow response to camera controls or having issues during camera boot.
  * Bugfix: LANC setup sometimes triggered IMU error on MōVI
* **v1.5.1**
  * Improvement: FIZ motor tuning profile adjustments
  * Bugfix: Camera Type setting on iOS and Android is now persistent on reboot

**MIMIC v1.5.1**

* Bugfix: API FIZ commands through MIMIC don't get forwarded to Movi with their full range
* Bugfix: Pressing "clear faults" in FIZ Axis Setup screen would not stop sending "clear faults" command until an all axis auto calibration is done or until MIMIC is reboot.

**Mobile Apps v1.5.x**

* New Feature: Majestic Span configurations to achieve whip pan
* New firmware bundle

**Known Issues**

* MIMIC may set range limits unintentionally. Check if you have limits set on FIZ screens in case you run into an issue where you can’t control FIZ.

