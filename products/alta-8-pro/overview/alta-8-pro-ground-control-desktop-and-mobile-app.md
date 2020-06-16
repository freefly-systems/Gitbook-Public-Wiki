---
description: Qgroundcontrol for ALTA 8 Pro
---

# ALTA 8 Pro Ground Control Desktop and Mobile App

Getting QGroundControl up and running is quick and easy! Use the ALTA Pro QGroundControl program to change ALTA Pro’s parameters, monitor statuses, and set up waypoint missions.

1. Download and install the application.
2. Start QGroundControl and ALTA Pro.
3. Connect your vehicle to the ground station device.
   1. WiFi
      1. To connect to ALTA Pro via WiFi, find the ALTA Pro’s WiFi connection by searching for it in your device’s WiFi menu and then connect to it like you would any other device.
      2. You may have to [enable the WiFi feature](https://docs.google.com/document/d/1imQvHqWrF_fCkm6sBj5LfYu820OBOBGOA25gjYavPF8/edit#heading=h.uwun58lkskht) on ALTA Pro if it is your first time connecting.
   2. 900/868MHz
      1. Simply plug in the 900/868MHz radio into your computer using the attached USB cable. If ALTA Pro is turned on the two radio’s will automatically connect!



![](https://lh4.googleusercontent.com/WZSO-Zy2pzTabJywexMqHJuPnKUsG-TFbRU-CffyqAHcu6tqtjh_ZjHqTp3KO9pGBkFeivkOiUxxesuy-qQnTsCeZYNsgmTVDQkI0dfWpH3B9CofvHFzANIRHKDSMvuVVsSpRHUR)

## **New Features**

**QGroundControl**

The implementation of QGroundControl into the ALTA Pro system results in new features.

1. By harnessing the full power of the  PX4 autopilot controller architecture, ALTA Pro has all the features of a modern drone: waypoints, autonomy, telemetry/C2, autoland, etc.
2. Advanced, high-bandwidth position hold offers unprecedented precision, repeatability, and stability.
3. PX4 integration will allow users to create and fly complicated waypoints missions with ease.
4. The use of Mavlink and Dronecode protocol makes drone software integration possible and creates straightforward path to custom sUAS solutions for both cinema and business.
5. ALTA Pro has a built in 900/868MHz radio which will allow for a range of up to 2 miles between the aircraft and ground station.

The ALTA Pro QGroundControl App will be actively maintained, and additional functionality may be added over time. For information on individual app updates, refer to the App release notes.

| ![](https://lh4.googleusercontent.com/OYWBgLsFrkKTzfbE5vUag7XudTmtdbHK4WF6Z_ZU8NTa8xqenvxSsJP5f9Mw9_mayEJsdcDeQuKUaVRnjmIir_Z0NuUUU_rBpuaj3RoNAZC0dsSE5pqYAO4QQlLK187d3EJxMRk4) | **For a more indepth review of QGroundControl’s capabilities and workflows, please visit the** [**QGroundControl User Guide**](https://docs.qgroundcontrol.com/en/)**.** |
| :--- | :--- |


| ![](https://lh4.googleusercontent.com/OYWBgLsFrkKTzfbE5vUag7XudTmtdbHK4WF6Z_ZU8NTa8xqenvxSsJP5f9Mw9_mayEJsdcDeQuKUaVRnjmIir_Z0NuUUU_rBpuaj3RoNAZC0dsSE5pqYAO4QQlLK187d3EJxMRk4) | **If you are currently operating with an ALTA \(Autopilot\) version, there is no need to upgrade if you’re happy with the current feature set. The Autopilot-controlled ALTA has an excellent track record for reliability and smooth flight characteristics. Currently, the Alta Autopilot version offers Orbit mode functionality and the Velocity clamp feature. While the ALTA Pro will continue to see features added, it is does not currently support Orbit mode and Velocity clamp functionality.** |
| :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <img src="https://lh3.googleusercontent.com/igD-0ZEIpq4VTWepKYuk6hVBGkMAa02ZjBzF2aM9wRKbge2gensB5BD9mSaB8sEbIGrSo-dqa6VUujXqvkk44-amU9_GDOXNT5_BodqvMsJKA7Xq40D0ZR8C_jsiXu4KzD0-MJzv"
        alt/>
      </th>
      <th style="text-align:left">
        <p><b>When flying multiple aircraft at the same time, take extreme caution to ensure that the aircraft connected to the laptop/mobile device is the desired craft. Failing to connect to the correct device may result in an inadvertently arming a aircraft or disarming one that is inflight.</b>
        </p>
        <p><b>We suggest not selecting &#x2018;Connect Automatically&#x2019; when using WiFi to connect to ALTA Pro and clearly labeling each 900/868MHz RX/TX pair.</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

900/868 MHz Radio

ALTA Pro makes use of a 900/868MHz radio to increase the communication range between the ALTA Pro and laptop ground station. This allows users to monitor, update, and reroute ALTA’s while up in the air or on the move.

| ![](https://lh3.googleusercontent.com/igD-0ZEIpq4VTWepKYuk6hVBGkMAa02ZjBzF2aM9wRKbge2gensB5BD9mSaB8sEbIGrSo-dqa6VUujXqvkk44-amU9_GDOXNT5_BodqvMsJKA7Xq40D0ZR8C_jsiXu4KzD0-MJzv) | **All 900/868MHz radio’s are set to default signal strength when they leave our facility. Users are responsible for making sure they are operating within the bounds of the radio communication regulations in their area. The radio strength settings can be updated with the** [**RFDTools**](https://goo.gl/16Gw5c) **program. Users will have to use the USB supplied with the radio modules to connect to their computer and update signal strength parameters. This should be done for both radios. Contact support for questions concerning how to update the radio settings.** |
| :--- | :--- |


## **QGroundControl Overview**

![](https://lh4.googleusercontent.com/6CcMTBGWMd3-bcAbJA6aLkHSAPU1nukflaIYypw2k3WziBIZrCRiVFYWL_DQbodEqnw1LP0RUUaaRlQ-gquM2TO7YmY4YKh0wdbqIaC3-b5QaZAnAD5bTSXB7VeHbSFjQT01MYO8)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Symbol</th>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Function</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/5kY76KXF7tkKG5UJEGQfTPynuGyhIWW4kyWtbbBidvxHogQE7KAY3UounBAEQRqVJ509FAEm43RgitjYGYfSeRCCxoW204a7gNAEwSZH8QlE-ge5SW0s6rbPCe2rnowj3WWDW_xe"
        alt/>
      </td>
      <td style="text-align:left"><a href="https://goo.gl/athtFe">Settings</a>
      </td>
      <td style="text-align:left">Configure the QGroundControl application.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh6.googleusercontent.com/PGdUD-dx-XXeB7-i6YbotZfBJIO7KCl7dpuHFiSNQJwb9f-NUNDSh5m_ZTUr0JqyFZgo3htxO_6ggFk0U7LWeFeOrc6KcGPn0r-Fg3rCzd2PDPcF8H2IZL-50k8qRp9ETnomheSX"
        alt/>
      </td>
      <td style="text-align:left"><a href="https://goo.gl/9bfMmw">Setup</a>
      </td>
      <td style="text-align:left">Configure and tune your vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/9ziSwhZjLomwVW_soGh5n0UsoZzQ1TLp6juR77pBbutDJZHqKpUw8-6JNA3XLVuFR64Bg0REA--FOJea1RteCtNV5kkO1yv_yC3CmluQxD0fA3zsvSRqltrErfRAJJTpAErwkuHl"
        alt/>
      </td>
      <td style="text-align:left"><a href="https://goo.gl/o8au7H">Plan</a>
      </td>
      <td style="text-align:left">Create autonomous missions.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh5.googleusercontent.com/jRkAffDQIIiVgENthwYwsCPfcDBI-dF2sNXqXy2QEFFjUUS0wrMUrtQLxSZdMkQzvScLMrYCsDOLPIcVuXzg0sFByxjZD-82jzGytbpKZeMaKG3ukZ0mKnxioH-PMEqabPYZeXgY"
        alt/>
      </td>
      <td style="text-align:left"><a href="https://goo.gl/7KnF8R">Fly</a>
      </td>
      <td style="text-align:left">Monitor you vehicle(s) while flying, including streaming video.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh5.googleusercontent.com/naKemY5oE0L5UZvS9vRDCMqpqMNMAnv4RVp7Qk3aQW5rwr7wXWWIfruhYV7bth6pf170oxM-Lugiwp7Z7UT1n3BcZ6dTXTyvj5kQYobg_ju1rhAOvlTExqWKBE-2gUXbn89OCJtN"
        alt/>
      </td>
      <td style="text-align:left"><a href="https://goo.gl/LF4tKm">Analyze</a>
      </td>
      <td style="text-align:left">Download logs, geotag images from a survey mission, access the MAVLink
        console</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh4.googleusercontent.com/VT7jdhaKvhmBxTO7uOpu43A8i4gC-Uho11MWaHAaDHbtSJ4EzkTrynBFl3xAclI8AitopoAkMbchb6J6sm1zIJ1hhdbwVOcd1fNpRNbBgDBm4BjUOHOngY2orShsDl4kToUvnfPw"
        alt/>
      </td>
      <td style="text-align:left">Vehicle Messages</td>
      <td style="text-align:left">Click to show a dropdown of messages from the vehicle. This will change
        to a Yield sign if there are critical messages. Yield sign shown in image
        above.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh5.googleusercontent.com/vyY_sJPaEFvrzfYBnC7D08bsMa-0JCzxo4-zrMuWoaAwvgD8GOJYMlGMKuIKwnLNy4y6UmeRw_fmB1Y9PNFgDibZRql5xjWzJUzl7N3J-C2Y4YsScNr7obYa3XDu6BywRDuKG0YD"
        alt/>
      </td>
      <td style="text-align:left">GPS Status</td>
      <td style="text-align:left">Shows you satellite count and current hdop.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh6.googleusercontent.com/dznST5gYzBowx1q28dsaglHD3k57NkCSfFDqUC7v5LOtyh49ZDdsTxELes7Qaf35P9tXz3ohlnq0Eerw_Kx-7JflmdH24FrGSnkS6120DDkeCTyGrNUUHV52caSVeZWPE7V6pvKz"
        alt/>
      </td>
      <td style="text-align:left">RC RSSI</td>
      <td style="text-align:left">RC signal strength information.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/dG_SLKI-F0jBIW2v_I6fDYYT1w7xvlFqKiu7PPQs_HUcOJo29gYSpLofjIw-a8Fr2la3bE3up6T8_n3UwJz9FZcXemKDQ9UOHOd8Ji21qt0pSF6g0Gk-80GAItuG_sMQKBQun5-X"
        alt/>
      </td>
      <td style="text-align:left">Telemetry RSSI</td>
      <td style="text-align:left">Telemetry signals strength information.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/bGvojkV1MKY5p7p1NZWzAFFDuTHEUEq0DgZZMoJq4jhIja22uCMOmXc7ldIKTZUiehH7P_j4ZAtkQyL3ovpzZ1hS1W19hWJ8mo9fcVrZOEEmbgO9QdFyzuZ4NrXvNqiQHUp9PLCl"
        alt/>
      </td>
      <td style="text-align:left">Battery</td>
      <td style="text-align:left">Remaining battery percent.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh5.googleusercontent.com/s440rYHch-bPsXDBbvb5UOW2MvSyjSZZMHtQgDcfpcVz-WSTKr4VNCBMDj-Ze7fonDM3vM2H_5QrShnAoALtMa0mR1_H-A2crwfLEP4SpnsdUD8-ujBY5pJadB9tpFT5rKGwhcId"
        alt/>
      </td>
      <td style="text-align:left">Flight Mode</td>
      <td style="text-align:left">Current flight mode. Click to change flight mode.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh4.googleusercontent.com/W_E4UjuYrzBjaBGqCvb1thBhULB7ModGMsD0J_Jt2wMUCArXAfcGiMINp7LE3BE-zfci23spXmkBehCX2j-yrwN3mwWoGCobwDbuqnxHR2pOY5PHllFBZrCjZaDt2mJ_dnH3x9a2"
        alt/>
      </td>
      <td style="text-align:left">RTK GPS Survey-In Status</td>
      <td style="text-align:left">
        <p>Shows you progress of RTK GPS Survey-In process.*</p>
        <p>*ALTA Pro does not ship with an RTK GPS</p>
      </td>
    </tr>
  </tbody>
</table>

## **ALTA Pro Specific QGroundControl Features**

### **Tuning Parameters**

QGroundControl has a custom tab that allows quick access to the most important ALTA Pro parameters. These parameters are accessible through the ‘Tuning’ tab in the Vehicle Setup Menu.

![](https://lh3.googleusercontent.com/eNCbkxTU9CJMwq3G8X3rHlYMn_1NwXXMxC8uvGIF_FbdeALpxuRtAkf05Q-zTERxP504ekofY8gfQ7iZSAggG2xQsqSQj3Zg7ePd8Uk2gwFitlwuJQvfYtHf35tqjnY11Y42jFb9)

### **ALTA Pro Parameters**

Access to boom LEDs and OSD parameters are also located in the Vehicle Setup Menu, under the Parameters tab and in the ALTA grouping.  


