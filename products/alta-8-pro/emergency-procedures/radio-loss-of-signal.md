# Radio Loss of Signal

### **Radio Loss of Signal \(LOS\)**

|  | Item | Action |
| :--- | :--- | :--- |
| 1. | Controller Battery | CHECK |
| 2. | Controller Antenna | REPOSITION |
| 3. | Mode Switch | POSITION |
| 4. | Home Switch | Return-to-Land |

Loss of Signal \(LOS\) can occur if the radio controller stops transmitting a signal, or if ALTA Pro is too far away to receive it. In the event ALTA Pro detects a LOS, it will automatically execute a Return-to-Land or Autoland as configured in ALTA Pro QGroundControl if using an S.Bus/S.Bus2 or DSM2/DSMX radio type. While ALTA Pro includes these emergency control modes, it is always recommended to attempt to regain signal link with ALTA Pro to keep the pilot in control of the aircraft.

Move the antenna orientation for best signal strength. Ensure the radio antenna matches the direction of the receiver antennas. Move the radio away from objects to get a clear line-of-sight to ALTA Pro.

Set the Mode switch to Position and the Home switch to Return-to-Land so ALTA Pro will continue to approach the home point if the signal is momentarily regained, resulting in higher likelihood of regaining full signal reception.

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **If efforts to regain control signal are unsuccessful, ALTA Pro will begin either the Return-to-Land and Autoland sequence as configured in ALTA Pro QGroundControl. Refer to the Flight Controller Modes section of this manual for additional information regarding functionality available with specific radio types.** |
| :--- | :--- |


