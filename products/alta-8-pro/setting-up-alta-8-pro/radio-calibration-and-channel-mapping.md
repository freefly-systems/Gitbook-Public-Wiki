# Radio Calibration and Channel Mapping

ALTA Pro can be used with a variety of radio controllers. Different radio controllers can map functions to different channels, so properly mapping controller channels to ALTA Pro functions is an important step before flying. Radio calibration and channel mapping are performed using the ALTA Pro QGroundControl program or app. 

If you are uncertain about your radio channel mapping, obtain assistance from an experienced pilot or from Freefly Customer Support. 

## Calibrating Radios Using ALTA Pro QGroundControl App

Calibrating any compatible radio is done using the ALTA Pro QGroundControl app. This only needs to be done when using a new radio with the ALTA Pro; ALTA Pros that were bought with a radio have already gone through the Calibration and Mapping procedures.

* Power the ALTA Pro by plugging in a USB-C cable to the expansion port. 
  * The expansion port is located under the closeout between booms 1 and 
* Once connected, the ALTA electronics will be powered and you may turn on the radio. 
* Open the ALTA QGroundControl program, navigate to the Radio tab in the Vehicle Setup menu, and then initiate the radio calibration.

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p></p>
        <ul>
          <li>
            <img src="https://lh4.googleusercontent.com/bPkNb0uGJf01_9S4NRCzx14N-NUHMfGqpk2GDZKvsHOC0TEqvbyeMwd1-JmoIqvsXpRd6iSvSVSkqcIvEsaytY1mq7DhdAcKUBaRYelz8pTcPy54V3ITJBf2mYm6kzjANyNLXB2S"
            alt/>
          </li>
        </ul>
      </th>
      <th style="text-align:left">
        <p></p>
        <ul>
          <li>Make sure to reset all trims and subtrims to zero before continuing with
            calibrating and mapping your radio.</li>
        </ul>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>*  Set the transmitter mode radio button that matches your radio configuration \(this ensures that QGroundControl displays the correct stick positions for you to follow during calibration\).
*  Move the sticks to the positions indicated in the text \(and on the radio image\). Press Next when the sticks are in position. Repeat for all positions.
*  When prompted, move all other switches and dials through their full range \(you will be able to observe them moving on the Channel Monitor\). 
* Press Next to save the settings. 

## Mapping Channels Using ALTA Pro QGroundControl App

Radio channel mapping is accomplished with the Alta Pro Qgroundcontrol App. Prior to mapping channels, ensure your radio controller and receivers are properly installed and calibrated. Refer to the Radio Installation section of this manual and your radio controller’s documentation.

* Power the ALTA Pro by plugging in a USB-C cable to the expansion port. The expansion port is located under the closeout between booms 1 and 2 
* Once connected, the ALTA electronics will be powered and you may turn on the transmitter.
* Open the ALTA QGroundControl program, navigate to the Flight Mode tab in the Vehicle Setup menu for access to the channel mapping.
* Channel mapping can be customized by the user on this menu to fit their preferences. Below is a quick description of the items mapped to the transmitter and suggested channels for each mapped item. 

## Function Descriptions 

The following functions can be mapped to radio controller channels. These are found in the Radio section of the Configurations menu in ALTA QGroundControl. Each function is also represented by a chart that responds to control input allowing for quick verification of mapping settings.

### Controller

Use this to select the appropriate receiver. The following guide is compiled for convenience. For complete specifications and which mode will work with your receiver, refer to your radio controller or receiver manuals. DSM2/DSMX are typically used by Spektrum controllers SBUS is typically used by Futaba controllers 

### Pitch/Roll/Yaw/Throttle

 The Pitch, Roll, Yaw and Throttle controls are the basic flight controls and are mapped to the two radio controller sticks. 

### Mode 

The required Mode Switch selects between the three different flight modes: Manual, Altitude, and Position. A three-position switch is recommended to select the three different modes. However, a two-position switch may be used, but will only allow for selecting between Manual Mode and \(depending on radio controller mixes\) either Altitude Mode or Height Mode

###  Return to Home Switch

The optional Return to Home Switch selects between the different Return-to-Land \(RTH\) functions. At minimum a two-position switch is required for the Home Switch functions to select between RTL Off, and initiate RTL functions.

## Typical Channel Mappings

 The following radio channel mapping configurations are recommendations only and can be set in ALTA QGroundControl. Depending on exact radio models, these may help as an initial configuration. However, it is up to the pilot setting up ALTA Pro for flight to determine if these settings are appropriate.

###  Futaba 14SG/8FG



| **Function** | **Channel Number** | **Direction** |
| :--- | :--- | :--- |
| **Pitch** | **2** | **Normal** |
| **Roll** | **1** | **Normal** |
| **Yaw** | **4** | **Normal** |
| **Throttle** | **3** | **Reverse** |
| **Mode Switch** | **5** | **Normal** |
| **Home Switch** | **6** | **Normal** |



![](https://lh3.googleusercontent.com/UbSNRPrXv0zdmyzyxJUR9jHZBPtDM7Amu642fBYbDMh5n7waCfyn7sevZSVTTdatCTVbZA7lSTlwhbjhqXuoDimWfLdUXv5O0DqGaFflperJTJtpav1nQi-tilx_LMMi_6hBMNnl)

### Spektrum DX18

 

| **Function** | **Channel Number** | **Direction** |
| :--- | :--- | :--- |
| **Pitch** | **3** | **Reverse** |
| **Roll** | **2** | **Reverse** |
| **Yaw** | **4** | **Reverse** |
| **Throttle** | **1** | **Normal** |
| **Mode Switch** | **6** | **Reverse** |
| **Home Switch** | **7** | **Normal** |



![](https://lh5.googleusercontent.com/Kou9JKcxar3v018LwTpLVYp6Jxx53g3POADchtadw1oNKwEewgQ62FmDgjWePzGqmgj2xrhQaqt4nZ6hzjMdnZwrJWTQkS1t1vLVOMY88z2qSIxmKbM_zBhjuKpnoaOojd5zvYce)

