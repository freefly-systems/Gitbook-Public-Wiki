# Software Release Notes



### **Compatibility**

{% hint style="warning" %}
MōVI **M5/10/15** is compatible with MōVI Controller firmware **v4.1.3 or below**

MōVI **Pro/XL/Carbon** is compatible with MōVI Controller firmware **v3.0.1 or above**
{% endhint %}

### \*\*\*\*

### **v4.2.0** 

* **Bugfix:** FIZ range limits were sometimes getting set randomly. This was causing it to look like a FIZ axis was getting stuck or locked.
* **Bugfix:** Movi Controller was occasionally sending corrupt gimbal commands, causing Movi to briefly twitch or reset its FIZ values
* **Bugfix:** Can’t select/unselect lenses from lens library
* **Bugfix:** Carbon wasn’t displaying units for FIZ in the FIZ main screen, due to the lens library not working.
* **Improvement:** Pan/tilt trim knobs can now be used in Wheels mode
* **New Feature:** Added reset attitude button under Movi Expert screen for use with Movi firmware v2.0.16 or above. Scroll to it in the menu, then turn the right knob right to initiate the process
* **Known issue:** Lens Library sometimes doesn’t save new lenses

### \*\*\*\*

### **v4.1.3** 

* **New Feature:** FRX Pro support! Go to Radio Config and change Radio Type from Internal to USB
* **Improvement:** Signal strength indicator in Radio Config when USB mode is selected \(for use with FRX Pro\) displays good/weak/bad instead of packets per second.
* **Bugfix:** Adding a new lens to lens library would freeze MōVI Controller even when rebooted.
* **Known issue:** Can’t select/unselect lenses from lens library. Adding a new lens doesn’t persist.



### **v4.0.0**

* **New Feature**: ****Blackjack support
* **New Feature**: Roll mapping option for Wheels!
* **Improvement**: Added 360 roll mapping for Rocker and Joystick. 
* **Improvement**: Timelapse menu is removed during winter clean up. App version is significantly improved.
* **Improvement**: Wheels advanced settings \(termination, LED, etc\) on Movi Controller
* **Improvement**: Added timeout features to Wheels
* **Improvement**: Display 0 values for joystick smoothing/window/expo when Wheels enabled.



### **v3.7.2**

* **New feature:** [Movi Wheels](https://store.freeflysystems.com/products/movi-wheels) support & TX Config screen updates
* **Improvement:** Iris and Focus linearization for MōVI Carbon and set crop factor, which now makes displayed lens range 40-240mm



### **v3.6.0**

* **New Feature:** Zoom Rate Scaling UI so users can adjust the Zoom Rate
* **New Feature:** Default the lens profile on MōVI Carbon to Fujinon XK 20-120mm.



### **v3.2.1**

* **Improvement**: Alpha Wheels Mode is improved and jitters are further eliminated. Some notes:
  * MIMIC settings no longer apply.
  * Joystick settings now apply. For the most direct feel, dual op pan and tilt joystick window, smoothing, and expo should be set to zero. They can be modified for more smoothing if desired.
  * Remote Rate Scale now applies and is a final drive ratio with the maximum of 200º/s. So, 70:1 wheels gear plus 100º/s Remote Rate Scale will be a total of 140:1 wheels to axis ratio.
  * Should work better with high Hold Strength. You will still get overshoot on abrupt stops. High Hold Strength puts more responsibility in the operator's hands for the start and stop ramps.
  * There is a known bug where the controller must boot in Alpha Wheels mode to initialize the wheels properly. Not addressed by this update. We'll look into it for next release.
  * If you are using MIMIC version of the Alpha Wheels, we recommend to get the latest firmware from [1A Tools](https://1a.tools/downloads/). 
* **New Feature**: Added Chrosziel CDM-100M Lens Motor option to the FIZ Axis config motor selection list.



### **v3.1.0**

* **Improvement:** Changed all references to "WEDGE" in displays to "FIZ"
* **New Feature**: Added Hocus Reflex to motor selection list
* **New Feature**: Added bare-bones Aux Port for API pass-through

