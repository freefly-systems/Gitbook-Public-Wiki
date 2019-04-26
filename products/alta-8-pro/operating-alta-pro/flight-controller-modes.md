# Flight Controller Modes

## **Flight Controller Modes**

### Overview

ALTA Pro has three primary flight control modes which are selected using the Mode Switch: Manual Mode, Altitude Mode, and Position Mode. ALTA Pro also has two emergency control modes, Return-to-Land and Autoland, which are available only during certain situations. For additional information, refer to the sub-section associated with each emergency control mode.

| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Altitude Mode and Position Mode are assistive only and are not a replacement for pilot skill and ability. Pilots should be proficient in Manual Mode flight in order to react to emergency situations as required.** |
| :--- | :--- |


| ![](https://lh4.googleusercontent.com/bPkNb0uGJf01_9S4NRCzx14N-NUHMfGqpk2GDZKvsHOC0TEqvbyeMwd1-JmoIqvsXpRd6iSvSVSkqcIvEsaytY1mq7DhdAcKUBaRYelz8pTcPy54V3ITJBf2mYm6kzjANyNLXB2S) | **Always center the control input sticks on the radio controller when switching between control modes to prevent unexpected movement of the ALTA Pro.** |
| :--- | :--- |


## **Manual Mode**

In Manual Mode, ALTA Pro will only stabilize its attitude. At neutral control input \(middle pitch and roll stick position\), ALTA Pro will attempt to remain level. Throttle control is direct.

## **Altitude Mode**

Altitude Mode changes the throttle stick behavior to command climb and descent rates. The higher the throttle stick position, the faster ALTA Pro will climb. Conversely, the lower the throttle stick position, the faster ALTA Pro will descend.

When the throttle stick is centered, ALTA Pro will enter Altitude Hold. In Altitude Hold, ALTA Pro will maintain a target altitude and try to correct for drift. If a disturbance moves ALTA Pro away from this target altitude, ALTA Pro will climb or descend to return to the target altitude.

| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Altitude Mode is assistive only and is not a replacement for pilot skill and ability. Pilots should be proficient in Manual Mode flight in order to react to emergency situations as required.** |
| :--- | :--- |


## **Position Mode**

Position Mode changes the pitch/roll stick behavior to command ground speeds. Pitch and roll stick deflection will command fore/aft and left/right ground speeds respectively. Controlling altitude in Position Mode is the same as in Altitude Mode.

With pitch and roll controls centered, ALTA Pro will enter Position Hold. In Position Hold, ALTA Pro will maintain its position over a given point on the ground and correct for disturbances.

Position Mode requires a strong GPS signal and communication with a minimum of 6 satellites. If a weak signal is present, ALTA Pro will not enter Position Mode. If the GPS signal degrades while in Position Mode, ALTA Pro will automatically revert to Manual Mode.

Within Position Mode ALTA Pro enters Classic Control style which use the tuning parameters to control translational position over the ground.  
****

| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Position Mode is assistive only and is not a replacement for pilot skill and ability. Pilots should be proficient in Manual Mode flight in order to react to emergency situations as required.** |
| :--- | :--- |


| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Flight using Position Mode in areas of degraded GPS signal, such as near buildings or under dense tree cover, is not recommended. The automatic reversion to Manual Mode can cause unexpected, abrupt changes in flight behavior.** |
| :--- | :--- |


| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Flight using Position Mode with Compass enabled in areas near large ferrous objects or high magnetic flux is not recommended. Incorrect compass readings can result in loss of control. Compass assist can be disabled in the ALTA App if desired.** |
| :--- | :--- |


## **Waypoints Mode**

Waypoints mode allows ALTA Pro to execute a predefined autonomous waypoint missions that have been uploaded to the flight controller via ALTA Pro QGroundControl \(QGC\). For more information on all of the different options and abilities built into the Waypoint functionality you can read more in the [PX Literature](https://goo.gl/i5PhEJ).

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **ALTA Pro must have a GPS lock on its home position in order to start a waypoints mission.** |
| :--- | :--- |


## **Return-to-Land**

Return-to-Land Mode will command ALTA Pro to fly back to the defined Home Point. When ALTA Pro first acquires a GPS position, it sets this as the Home Point of the flight. See the Radio Channel Mapping section in this manual for more information on setting up the Return-to-Land Switch.

RTL can be initiated automatically with an LOS event if it is selected as the Signal Loss Action in the ALTA App. RTL can also be initiated manually while flying in Position Mode and setting the Home Switch to RTH.

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **Full functionality of the PX4 LOS features is only available on an S.Bus/S.Bus2 or DSM2/DSMX receiver.** |
| :--- | :--- |


When initiated manually using the Home Switch, ALTA Pro will fly back to the Home Point. ALTA Pro will hover above the home point and wait for a set amount of time and then land. The pilot can cancel the RTL procedure by returning the Home Switch to the middle or bottom position.  
  


During an LOS event, RTL followed by Autoland will be initiated automatically if ‘RTL’ is selected as Signal Loss Action in the ALTA App and an S.Bus/S.Bus2 or DSM2/DSMX radio system is in use. ALTA Pro will first check its current altitude against Safe Height. If ALTA Pro is below the Safe Height, it will climb to Safe Height. If ALTA Pro is above Safe Height, it will remain at its current altitude. Next, ALTA Pro will fly back to the home position at the RTL Speed set in the ALTA Pro QGroundControl. Finally, upon reaching the home position, ALTA Pro will loiter for 15s and then begin to Autoland.

![](https://lh3.googleusercontent.com/jGl7I8mxa2RZXe0K6eRdGQ7dxBtYThMx1_GQKdNiwa_ECZi7G5AgQ2laMWj_WSKbBJmIp1wlbOFyoyzmOYRO0YBmkho7BVckTDKPhkb2sdXKJHQeUaVQv1SkNp7mX1lavYYK7g5v)

## Autoland

Autoland will only initiate if one of the following conditions is met and the Autoland is setup as the failsafe for these events. See the Safety Parameters to customize ALTA Pro’s failsafe behaviors:

* Loss of Signal \(LOS\) occurs and ‘Land’ is selected as the Signal Loss Action in the ALTA app
* At the end of a LOS Return-to-Land event when using S.Bus/S.Bus2 or DSM2/DSMX radio systems
* Battery exhaustion failsafe is tripped and the failsafe is set to return to land in ALTA Pro QGroundControl.

| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Autoland and Return-to-Land will only occur if these settings are turned on in the aircraft parameters.** **Geofences** |
| :--- | :--- |


## **Geofences**

Geofences are currently not supported by Freefly. We recommend that you do not use this feature. If this feature is used, set the Geofence breach action to Warning; Hold, RTL, and Terminate should not be used as they may result in crash or an ALTA Pro that cannot return to its home position.



