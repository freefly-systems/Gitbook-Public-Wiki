# Technical Specs

## Powerplant

|  |  |
| :--- | :--- |
| Number of Motors | 4 |
| Motor Max Continuous Power Output | 100 A |
| Motor Max Instantaneous Peak Power Output | 130 A \(&gt;3s\) |
| Equivalent Kv | 115 rpm/V |

## Propellers

|  |  |
| :--- | :--- |
| Material | Carbon Fiber Reinforced Nylon |
| Propeller Orientation | \(2x\) CW and \(2x\) CCW Props |
| Propeller Type | Folding - 840 x 230 mm \(33 x 9in\) |

## Battery

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Cells</td>
      <td style="text-align:left">12S</td>
    </tr>
    <tr>
      <td style="text-align:left">Nominal Battery Voltage</td>
      <td style="text-align:left">44.4V</td>
    </tr>
    <tr>
      <td style="text-align:left">Charged Battery Voltage</td>
      <td style="text-align:left">50.4V</td>
    </tr>
    <tr>
      <td style="text-align:left">Battery Connectors</td>
      <td style="text-align:left">XT-90</td>
    </tr>
    <tr>
      <td style="text-align:left">Required Minimum Battery Discharge Rating (Per Pack)</td>
      <td style="text-align:left">
        <p>320 Amps per battery</p>
        <ul>
          <li>(assumes two batteries) 20C for a 16A-hr pack.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>## Weight

|  |  |
| :--- | :--- |
| Maximum Gross for Takeoff | 34.9kg |
| Maximum Payload | 15.9kg |
| Typical Standard Empty Weight | 10.4 kg |

## Flight Controller

|  |  |
| :--- | :--- |
| Autopilot Name | Custom Auterion PX4 flight control stack |
| Flight Modes | Manual, Altitude, Position, Mission, Loiter, Orbit, Return |
| Supported Inputs | MAVlink SDK |
| Supported Radios | Futaba, Spektrum, PX4 compatible SBUS and PPM receivers |
| Supported Radio Controller Telemetry Systems | Voltage feed provided for Futaba RX telemetry |
| Minimum Radio Controller Channels Required | 5 \(roll, pitch, yaw, throttle, mode\) |
| Supported GNSS | GPS/Glonass/Beidou/Galileo |

## Lighting and Indication

|  |  |
| :--- | :--- |
| Orientation Lights | Boom tip mounted LEDs |
| Orientation Light Color Options | User controlled in software - red, orange, yellow, green, cyan, blue, purple, white, and off. |
| FPV Ability | Yes, see the FPV integration section for instructions on how to mount the FPV. |

## Isolation Systems

|  |  |
| :--- | :--- |
| Vibration Isolation System | Built-in _\(see chart below for weight suggestions\)_ |

| Payload \[lb\] | Payload \[Kg\] | Isolator Durometer | Cartridge Qty |
| :--- | :--- | :---: | :---: |
| 0 - 3 \* | 0 - 1.4 | 30A | 3 |
| 4 - 10 \* | 1.8 - 4.5 | 30A | 6 |
| 11 - 19 \*\* | 5.0 - 8.6 | 30A | 9 |
| 20 - 23 \*\* | 9.1 - 10.4 | 30A/40A | 9 |
| 24 - 29 \*\* | 10.9 - 13.2 | 40A | 9 |
| 30 - 32 \*\* | 13.6 - 14.5 | 40A/50A | 9 |
| 33 - 35 \*\* | 15.0 - 15.9 | 50A | 9 |

