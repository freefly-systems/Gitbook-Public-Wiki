# Software Release Notes

## Intro

ALTA QGroundControl is based on the public version of the [QGroundControl](http://qgroundcontrol.com) and is tailored for use with ALTA X and ALTA 8 Pro. Although you should be able to use the public version, we highly recommend using the Freefly version to be fully compatible. Freefly only uses and tests the ALTA QGroundControl.



## v1.3

* **Summary**: Support for RTK
* **Release Date**: March 2020
* **Versions in this package**: 
  * Windows: v1.3.8
  * Mac: v1.3.8
  * iOS: v1.3.8
  * Android: v1.3.8
* **Notes**:
  * New Feature: RTK status indicator and button to restart survey-in \(Windows and Mac only\)
  * New Feature: Display ALTA firmware version numbers in QGC
  * Improvement: Disabled QGC version check complaints
  * Improvement: Warn when advanced parameters screen is open
  * Improvement: Lockout feature
  * Bugfix: Airframe name doesn't display ALTA X
  * Bugfix: Hide MPC\_CRUISE\_90 and MPC\_DEC\_HOR\_SLOW for ALTA X on ALTA Config screen \(not available with v1.2 firmware\)

## v1.1

* **Summary**: Support for ALTA X
* **Release Date**: September 2019
* **Versions in this package**: 
  * Windows: v1.1.4
  * Mac: v1.1.4
  * iOS: v1.1.4
  * Android: v1.1.4
* **Notes**:
  * New: ALTA X support
    * Support for PX4 firmware v1.9
    * Allow for multiple airframe parameter defaults
    * Number of LEDs displayed on config screen
  * Improvement: Display a warning if switching airframes while the app is open

## v1.0

* **Summary**: Initial release for ALTA 8 Pro
* **Release Date**: April 2019
* **Versions in this package**: 
  * Windows: v1.0.6
  * Mac: v1.0.6
  * iOS: v1.0.6
  * Android: v1.0.6
* **Notes**:
  * ALTA QGroundControl v1.0.6 is based on Public QGroundcontrol v3.5.1 stable
  * Included new parameters we added for ALTA support such as LEDs and OSD 
  * Overwrote their Tuning screen with our own to include frequently used parameters. This is to make it more convenient to user compared to going to all parameters screen where parameter names are cryptic and only provides basic UI. 
  * Overwrote their parameter defaults to match ALTA defaults 
  * Moved a component in radio screen to make it not crop for small screens 
  * Overwrote app name and version number so that app can be differentiated from the public one 
  * Removed "Reset all to defaults" for UX purposes. This button ends up kicking you out of wifi and erasing all calibration values 
  * Adding parameter file import/export functionality for iOS and Android



## v1.5 Beta

* **Summary**: 3D Mission Viewer Beta
* **Release Date**: September 2019
* **Versions in this package**: 
  * Windows: v1.5.1
  * Mac: n/a
  * iOS: n/a
  * Android: n/a
* **Notes**:
  * This is a beta release and it is for windows only. Full details can be found at this [link](https://docs.google.com/document/d/121KmrEYxuvnf8b9IP5jkid9pv9oSciSi6_fwqriyVQI/edit?usp=sharing).
  * New: 3D Mission Viewer

















