# User Interface

## Module LED Indicators

The RTK GPS modules have two different LED indicators: multi-color status LED and red, safety LED.

### Multicolor \(RGB\) Status LED

This LED is located in the corner of the modules, and can vary in color.

When installed on AltaX \(or another PX4-based autopilot\), the LED follows PX4 convention: [https://docs.px4.io/v1.9.0/en/getting\_started/led\_meanings.html](https://docs.px4.io/v1.9.0/en/getting_started/led_meanings.html)

![](../../.gitbook/assets/led_meanings-1.gif)

On the base station, the LED lights solid white when the module is powered via USB.

### Red Safety LED

This LED is located next to the module's button.

When installed on AltaX, the LED indicates arm status

* Double-blinking red: aircraft is powered up, but not armed
* Solid red: Aircraft is armed

On the base station, the safety LED is used to indicate bootloader mode \(used for firmware updates\). The LED will briefly blink when the module is first powered up via USB, and will stay solid red when the module is in bootloader mode.

## Alta QGroundControl GUI

When the base station is plugged into your computer, Alta QGC will display two GPS-related indicators:

* **Aircraft GPS**: This is the same dialog as with normal GPS, and it indicates:
  * **GPS Count**: The number of satellites seen by the **Alta**
  * **GPS Lock**: The type of lock.
    * 3D GPS = normal \(non-RTK\)
    * 3D RTK GPS Lock \(fixed\) = RTK lock, best precision
    * Other modes:
      * 3D RTK GPS Lock \(floating\) is pretty much equivalent to 3D GPS
      * 2D GPS is equivalent to not having GPS \(ie, it must be at least 3D to be of any use to the aircraft\)
  * **HDOP**: Horizontal Dilution of Precision: A measure of how good the horizontal position is \(lower is better\)
  * **VDOP**: Vertical Dilution of Precision: A measure of how good the vertical position is \(lower is better\)
  * **Course over ground**: Direction of flight path. Only valid when the aircraft is moving

![Aircraft GPS Status](../../.gitbook/assets/qgroundcontrol_rgtouwitkw-copy%20%282%29.png)

* **RTK Base Station**: This icon and window indicates the status of the base station

  * The RTK icon color indicates status:
    * Red or Grey: Not connected, no base station GPS detected
    * Blue: Survey-in initializing
    * Yellow: Survey-in active
    * White: Survey-in complete, base station is sending RTK corrections
  * GPS Status \(inside the window when the icon is clicked\) indicates the Survey-in Status
    * Not Connected: No base station GPS detected
    * Survey-in in process
    * Survey-in complete: Base station is providing RTK corrections, aircraft can compute RTK lock
  * **Accuracy**: Current accuracy of position estimate. Accuracy number should decrease during survey-in, and will remain the same after survey in is complete
  * **Satellites**: Number of satellites observed by the ground station. This number might not match the aircraft's number
  * **Duration**: Duration of survey-in. Number will increase until survey-in completes
  * **Lat/Lon**: Computed Global location of base station
  * **Alt**: Altitude computed by base station

![Base Station status showing survey-in in process](../../.gitbook/assets/image%20%2829%29.png)

![Base Station status showing survey-in complete\`](../../.gitbook/assets/image%20%2811%29.png)



