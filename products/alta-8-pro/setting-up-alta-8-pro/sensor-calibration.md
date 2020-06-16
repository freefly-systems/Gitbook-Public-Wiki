# Sensor Calibration

ALTA Pro features a highly sensitive 3-axis magnetometer, gyroscope, and accelerometer that measure specific force, angular rate, and earth’s magnetic field to infer heading and maintain stability. Occasionally, the sensors will require recalibration.

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **ALTA Pro’s compass should be regularly calibrated, especially when traveling between different geographic locations. For best results, it is recommended to perform manual compass calibrations away from ferrous objects, buildings and vehicles. In addition, concrete can contain steel rebar which may influence compass calibrations** |
| :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <img src="https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c"
        alt/>
      </th>
      <th style="text-align:left">
        <p><b>Perform calibration without a payload attached and all motor booms extended and latched. Folded booms will cause an inaccurate calibration.</b>
        </p>
        <p><b>It is recommended to use two people to perform the compass calibration as it requires handling and rotating ALTA Pro.</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

## **To perform sensor calibrations on ALTA Pro:**

1. Mount a pair of batteries onto ALTA Pro.
2. Plug in the batteries to power up the aircraft.
3. Open the ALTA Pro QGroundControl and connect to ALTA Pro.
4. Navigate to the Sensors tab under Vehicle Setup.
5. Available sensors are displayed as a list of buttons beside the sidebar. Sensors marked with green are already calibrated. Sensors marked with red require calibration prior to flight.
6. Click on the button for each sensor to start its calibration sequence and follow the instructions provided in the ALTA Pro QGroundControl.
7. Start by selecting Set Orientations and set the autopilot orientation
   1. Autopilot Orientation: ROTATION\_YAW\_270



![](https://lh6.googleusercontent.com/_CPpt6AHyWQBGx3gHYrDJogi_eMM3FNDvAdBs89HN59DhOJhvsCBkdwOOQaS3bR_hIPT3dgH6ZFYURyuxQXCpQXua0tI2kTWVcS4UhsEzkW_58uMzc8_ccYpTOCHfyyyx7HVG_QX)



![](https://lh4.googleusercontent.com/i2cSN8GsQ7jqizDzjWR6u6vVwdIiDyaCqoHemifixPSi0Tv1vBhbvLtX9BWRaqJMHrOef-r7lrf-vLYvMkzi4W9pQoV9hKTA-VTHUmaaQCQq1xibQGY0TRi0Z2cI1nXAaVaUf9h4)



![](https://lh3.googleusercontent.com/JVm8LtapY3rocOkO8vwE8C6mJrAfQjhJZsKEw6cMEw4PI9F0PekEpyta8OCb0hRZNxxrET9QJOkbGT618kFSgXcN-hXj0lZyO1iGeABi-kxEODHb46_yI18J-Q1H4oYWKMPQGQTX)

## **Compass Calibration**

Follow the instructions below to perform a compass calibration on ALTA Pro. Compass calibrations should be done when flying in a new location or when ALTA Pro QGroundControl prompts a calibration.

1. Click the Compass sensor button.
2. Click OK to start the calibration.
3. Place the vehicle in any of the orientations shown in red \(incomplete\) and hold it still. Once prompted \(the orientation-image turns yellow\), rotate the vehicle around the specified axis in either/both directions. Once the calibration is complete in that orientation the associated image on the screen will turn green.
4. Repeat the calibration process for all vehicle orientations.

![](https://lh4.googleusercontent.com/GGjKbsICPSKW3rZlPqzndOb-4DvTROZQc8uJmrP8AtrV6RgmyjxCuG3cGCKnSdFkDdcvQXZhm9GQbcR6y79LVkkBJKrczEEmSgDIZ_TPFC6XWAm0krHk6nvKNrh88fEx_4_SR6jo)

## **Accelerometer Calibration**

Follow the instructions below to perform an accelerometer calibration on ALTA Pro. Accelerometer calibrations should only be done when prompted by ALTA Pro QGroundControl.

1. Click the Accelerometer sensor button.
2. Click OK to start the calibration.
3. Position the vehicle as guided by the images on the screen. This is very similar to compass calibration.

![](https://lh5.googleusercontent.com/GZWNVEtj_ifyjjNivjjfhLMjcm4rrESRQBH6F5N4kBBViWbz-S9-AUcHVqEdgIB4sAsLNkxC3-HH3bLYYsfg5dl2Y5TJrFoN11n9Es3eIy5kNNgyG92srBwRxv4wJLJRoMWokEpZ)



## **Level Horizon Calibration**

Follow the instructions below to perform a level horizon calibration on ALTA Pro. Horizon calibrations should only be done if the horizon \(as shown in the HUD\) is not level after completing Accelerometer calibration.

1. Click the Level Horizon sensor button.
2. Place the vehicle in its level flight orientation on a level surface.
3. Click OK to start the calibration.



