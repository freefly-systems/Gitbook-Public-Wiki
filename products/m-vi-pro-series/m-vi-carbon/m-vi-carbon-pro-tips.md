---
description: >-
  Here are the most common issues and mitigation strategies for Carbon
  customers.  As always Freefly support is here to help if you run into issues!
---

# MōVI Carbon Pro Tips

### Key links

* [Quick Start Guide](https://docs.google.com/document/d/1q0S6bYa0j7KNIPyDE6ysQRg82Gj7m3edNHMcPU4ZzFY/edit#heading=h.plkj0nqr3ski)
* [Manual](https://docs.google.com/document/d/1Qj879QV_canraQmIV7_-zamYaQdCsQ-leps5wR1DZRc/edit)
* [Customer Support](mailto:support@freeflysystems.com)

### Software

* You need to be running Movi firmware v2.0.10 or above for FRX Pro to work
  * Movi Controller \(MC\) will need to be on v4.1.3 or above with this package
* Carbon does not need to be autotuned and then gains / filters do not normally need any adjustment
* If you run a joystick pan/tilt window of &lt; 4 on the MC you will start to see joystick noise in the image
  * Additionally, if you are using FRX Pro on the MC, make sure that it is getting power from an external power supply, as noted in the [Using FRX Pro](../../frx-pro/how-to-use/) section of the wiki.
* The Carbon IMU takes several minutes to reach peak performance, but it is fine to shoot with it in this time
* The Carbon IMU has a max rate of 200 deg / sec. If you exceed this it will corrupt the attitude estimate and roll / tilt / pan could drift. If this happens please activate the new “Reset Accel” option in the app / MC. This will temporarily tell Carbon to ignore the gyros and listen to the accelerometer to level itself. It's important to be stationary and not accelerating when using this feature.
  * If you operate Carbon with full pan / tilt rate you will need to be gentle on the joystick or you can get some interaction / slapping with the inner / outer axis.  Right now the acceleration limits are not working properly on the inner axis. Alternatively if you absolutely do not want this to happen you can reduce the pan speed or reduce the remote scale to a value of 150 deg / sec or less
* Make sure you power down your camera when you change settings so you do not lose them when you turn Carbon off.  

### Mechanical

* You do not need to balance Carbon, it comes pre balanced from Freefly.
* If you add accessories to Carbon you will need to adjust pan balance, this is the only adjustment you will need to make
* Carbon needs to have either a UV filter or a ND filter in place to balance properly
* Please do not adjust the inner axis, the balance is precisely set at the factory and it takes special equipment to achieve the level of balance needed for Carbon to perform at full zoom
* To check pan balance, tip Carbon to the side and see if Pan swings forward / backwards - adjust as needed to prevent this

### Support

* If you do have an issue that you cannot solve please provide the following.  With these items Support can solve the issue 10x faster than with just a text description
  * Video of the behavior
  * List of your setup \(with FWs running on each item\)
  * Log file of the behavior

