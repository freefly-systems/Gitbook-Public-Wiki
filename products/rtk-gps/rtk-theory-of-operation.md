# RTK Theory of Operation

## General RTK Procedure

The RTK system requires two GPS modules:

* The Base Station GPS should be mounted in a stable location on the ground.
  * During the survey-in period, it observes its location and averages it to acquire a very accurate estimate of its absolute location on earth. The longer the survey-in, the more accurate the location will be.
  * After the survey-in period, the base station GPS will broadcast GPS corrections to the Rover, which can use the corrections to calculate an accurate absolute location.
  * **Note**: For optimal performance, the base station GPS should not be moved after survey-in has begun!
* The Rover GPS is mounted on the aircraft, and receives corrections from the base station to calculate very accurately its location.
* Additional components are required for the system to work:
  * Ground station computer & software \(Alta Ground Station\)
  * Communications link to aircraft \(such as FRX Pro\)
  * PX4-based autopilot
  * The standard signal flow is the following:
    * The base station GPS sends correction data to the ground station software
    * The ground station software sends the correction data to the aircraft's PX4-powered autopilot
    * The autopilot forwards correction data to the Rover GPS
    * The Rover GPS calculates its accurate location, sends it back to the PX4 autopilot



![](https://blobs.gitbook.com/assets%2F-LaNHxABbg20hfA0zTDQ%2F-M0ZhlZfsRCEzwLVcxJM%2F-M0Zi03_WPANMoS3Q53t%2Fimage.png?alt=media&token=f68de584-c757-45ea-a8c0-3509f84a73a1)





## Base Station Notes

For best performance, please note the following:

* Install the base station on a stable mount
* Do not move the base station once survey-in has begun
* Place the antenna in an location with as much sky view as possible. The more sky the GPS can see, the more satellites, the faster the lock, the faster the survey-in
* Survey-in will begin as soon as it is plugged into the computer and the ground station software is started



## Survey-in Process

Survey-in is the process where the ground station GPS sits stationary and performs many measurements to improve its location estimate. In essence, over time, any errors will average out and the estimate error will decrease. This survey-in period is critical, since it will determine the overall accuracy of the aircraft.

During the survey-in, Alta QGC will display the mean 3D error, and you should notice it steadily decreasing. Survey-in is complete when both of the following criteria are met:

* Mean 3D error is below a pre-defined threshold \(Alta QGC default is 2m\)
* Minimum observation time has been met \(Alta QGC default is 180s\)

After survey-in, the base station GPS will start broadcasting packet in the "RTCM3" standard, which the aircraft \("Rover"\) GPS utilizes to calculate very accurate positional data. The process of the Rover establishing high-accuracy position does take a few seconds after survey-in is complete, and will be indicated by a GPS status of "RTK \(fixed\)."

It's critical that the base station is not moved, either during survey-in, or after. Every time you move the base station, you should restart survey-in, which can be done by pressing the button "Restart" in the "RTK" window on the main toolbar.



![](https://blobs.gitbook.com/assets%2F-LaNHxABbg20hfA0zTDQ%2F-M0ZhlZfsRCEzwLVcxJM%2F-M0Zi03_WPANMoS3Q53t%2Fimage.png?alt=media&token=f68de584-c757-45ea-a8c0-3509f84a73a1)

## 

