# Troubleshooting



### **General Warnings**

| Symptom | Potential Cause | Potential Solution |
| :--- | :--- | :--- |
| Boot Fail | Voltage limits exceeded | Check voltage of flight packs and replace as necessary |
| Compass readings out of limits | Check surroundings and boot in an area away from ferrous objects. Recalibration of the compass. |  |
| Compass Warning | Invalid compass calibration | Calibrate the compass |
| GPS Warning | GPS/Compass Unit has become disconnected | Check the GPS/Compass unit wiring for damage |
| Accelerometer Warning | Hard landing | Reboot ALTA Pro |
| Motor Warning | ESC or Motor failure or error | Contact Freefly Customer Support immediately. Do not continue flying ALTA Pro. |



## **Flight Controller**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Symptom</b>
      </th>
      <th style="text-align:left"><b>Potential Cause</b>
      </th>
      <th style="text-align:left"><b>Potential Solution</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">ALTA Pro will not arm</td>
      <td style="text-align:left">Radio not bound</td>
      <td style="text-align:left">Follow radio controller manufacturer&#x2019;s binding procedure</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Radio not mapped properly</td>
      <td style="text-align:left">
        <p>Check radio mapping charts for correct behavior.</p>
        <p>Adjust mapping as necessary in ALTA Pro QGroundControl</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Flight Controller boot not successful</td>
      <td style="text-align:left">
        <p>Power cycle ALTA Pro. Ensure it does not move during boot</p>
        <p>If ALTA Pro must move during boot (such as on a moving platform), use
          Motion Booting</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Low Battery</td>
      <td style="text-align:left">A low battery error latches and does not allow further take off without
        a battery replacement.</td>
    </tr>
  </tbody>
</table>

#### **Flight Behavior**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Symptom</b>
      </th>
      <th style="text-align:left"><b>Potential Cause</b>
      </th>
      <th style="text-align:left"><b>Potential Solution</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Unexpected flight behavior</td>
      <td style="text-align:left">Tuning too high or too low</td>
      <td style="text-align:left">
        <p>Revert tuning to the last known working configuration</p>
        <p>Set tuning back to default values</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro does not maintain level pitch or roll</td>
      <td style="text-align:left">Pitch or Roll Trim position not set</td>
      <td style="text-align:left">Use the ALTA app to set the appropriate pitch and roll trim</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro oscillates or vibrates during flight</td>
      <td style="text-align:left">Tuning too high or too low</td>
      <td style="text-align:left">Check flight settings and tuning parameters in the App. Revert tuning
        to the last known working configuration. Re-tune.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Propellor Damage</td>
      <td style="text-align:left">Check for damage to propeller blades. Replace with spares as required.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Propeller blades unbalanced</td>
      <td style="text-align:left">Replace with spares as required. Propeller blades are balanced and matched
        at the factory.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Hinge or motor misalignment</td>
      <td style="text-align:left">Thoroughly inspect ALTA Pro following any accident. Contact Freefly for
        further inspection and assessment.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Ice on Propellers</td>
      <td style="text-align:left">Ice build-up is causing vibrations due to unbalanced propellers. Remove
        ice from propellers before further flights.</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro is sluggish in response to commands</td>
      <td style="text-align:left">Tuning too low</td>
      <td style="text-align:left">Check tuning in ALTA Pro and adjust as required</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Flight weight is over limit</td>
      <td style="text-align:left">Weigh the ALTA Pro and compare to the Allowable Gross Weight table in
        this manual. Remove weight.</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro ascends or descends when switching between flight modes</td>
      <td
      style="text-align:left">Hover Throttle set incorrectly</td>
        <td style="text-align:left">Follow the instructions listed in the ALTA Pro Flight Parameters section
          of this manual to adjust Hover Throttle</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro does not maintain heading</td>
      <td style="text-align:left">Yaw during boot</td>
      <td style="text-align:left">Re-initialize ALTA Pro while keeping ALTA Pro stationary in all directions</td>
    </tr>
    <tr>
      <td style="text-align:left">Unexpected behavior in Position Mode</td>
      <td style="text-align:left">Position lock not achieved</td>
      <td style="text-align:left">Monitor ALTA Pro QGroundControl and takeoff only after Position Lock has
        been achieved with strong GPS signal</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Incorrect heading due to yaw during boot</td>
      <td style="text-align:left">Re-initialize ALTA Pro while keeping ALTA Pro stationary in all directions</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Compass corruption or calibration</td>
      <td style="text-align:left">Check surroundings for ferrous objects or magnetic interference. Calibrate
        the compass. Disable the compass assist in the ALTA Pro QGroundControl.</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro circles a point in Position Mode</td>
      <td style="text-align:left">Compass calibration is invalid</td>
      <td style="text-align:left">Calibrate the compass</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Position tuning values too high</td>
      <td style="text-align:left">Reduce Position tuning values very slightly following the PX4 tuning guide.</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro does not track straight in Position Mode</td>
      <td style="text-align:left">Compass calibration invalid</td>
      <td style="text-align:left">Perform a manual compass calibration. Disable compass assist in the ALTA
        App if location has high magnetic flux or large ferrous objects</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro does not Return-to-Land when commanded</td>
      <td style="text-align:left">Position Lock not achieved</td>
      <td style="text-align:left">Monitor the ALTA Pro QGroundControl to ensure position lock has been achieved
        with strong GPS signal</td>
    </tr>
    <tr>
      <td style="text-align:left">Incorrect initiation</td>
      <td style="text-align:left">Incorrect initiation process</td>
      <td style="text-align:left">Set Mode switch to Position Mode. Set Home switch to RTL.</td>
    </tr>
    <tr>
      <td style="text-align:left">ALTA Pro wobbles when descending</td>
      <td style="text-align:left">Vertical descent into turbulent air from propellers</td>
      <td style="text-align:left">Descend at a slight angle relative to vertical so the ALTA Pro does not
        fly into turbulent air from propeller downwash</td>
    </tr>
  </tbody>
</table>