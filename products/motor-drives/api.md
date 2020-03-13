# API

## Overview <a id="API-Overview"></a>

Movi Pro API: [https://freeflysystems.com/support/movi-pro-support](https://freeflysystems.com/support/movi-pro-support)

At this time there is no API software written specifically for the Motor Drive project. The QX protocol is the same as that used in Movi Pro's API so that QX module can be used for motor drive. This page outlines the QX messages that you will want to send to control or monitor the drive.

You can communicate with Freefly motor drives over the QX Protocol, a custom communication protocol outlined on this page. This will allow for basic control of the drive as well as monitoring telemetry.

Freefly's customer support team prioritizes end-user support and will not be able to answer API support requests. Please visit the [Freefly Forum API Section](http://forum.freeflysystems.com/index.php?forums/m%C5%8Dvi-pro-api.65/) for FAQs, additional resources, and bug reports.

## Communication Channels <a id="API-CommunicationChannels"></a>

Each drive model may feature slightly different communication channel configurations:

* Arc 200:
  * CAN-bus, 1mbps
  * USB over ST virtual serial port driver: baud rate, parity, etc. do not matter over this emulated layer
  * External UART: 115,200kbps, 8 bits, no parity, 1 stop bit \(8N1\)

## QX Protocol <a id="API-QXProtocol"></a>

Freefly’s custom communications protocol that provides this interface is called the “QX Protocol”. This is a compact, lightweight binary messaging protocol that minimizes the size and complexity of messages, making it efficient for transmission on bandwidth constrained communications links.

Source code that allows building and parsing messages with this protocol is provided as a portable pure C language library that can be included in C/C++ projects directly, and used as a template in projects of other languages.

The QX protocol uses a client - server model where clients send read or write requests and receive current values, and servers send current values and receive read or write requests. In the Freefly API, the device connected to a COM port acts as the client and the MōVI Pro acts as the server.

## Configuring Motor Drive for API Control <a id="API-ConfiguringMotorDriveforAPIControl"></a>

To use the API on any of these channels, the drive just needs to be set in QX command mode. Set the 'Input Throttle Mode' configuration field to 'QX \(GUI, UART, CAN, BTLE, or API\)' and it will accept commands over this channel.

You can still use the QX communications over any channel to monitor drive telemetry even if the command mode is not in this mode. For example if you want to use an analog throttle but monitor drive temperature over QX, just set the input throttle mode to Analog and you can still monitor the temperature. You would not be able to command torque over QX anymore as the drive will only be listening to the analog throttle for commands.

## QX Over CAN <a id="API-QXOverCAN"></a>

To send a QX message over the CAN bus, you just need to send CAN message ID 0x78 with a payload length of 1 to 8 bytes. These bytes will be sequentially read into a QX parser. If a QX message is longer than 8 bytes \(as most are\), then you just send it in multiple 0x78 packets. For example if your message to send is 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, you would send a 0x78 ID CAN message of length 8 with payload 0, 1, 2, 3, 4, 5, 6, 7, followed by another 0x78 ID CAN message of length 2 with payload 8, 9.

There is nothing special about matching your QX messages to the frames of the 0x78 message. This is really just acting as a virtual UART layer on the CAN bus. Any 0x78 message is merely bytes coming in through the virtual UART stream which are then processed in the order received by the QX parser.

## QX Transmission Structure for API Access <a id="API-QXTransmissionStructureforAPIAccess"></a>

Here are the contents of the QX protocol. If you are using the QX submodule included with the Movi Pro API, you probably won't need to craft these messages at the byte-level. If you are implementing your own QX handler you will need to send a message that follows this structure. The response will come back from the drive in the same structure appearing as another QX message of the same attribute ID.

| Offset | QX Purpose | Value/Range | Data Function |
| :--- | :--- | :--- | :--- |
| 0 | Header 'Q' | 'Q' = 0x51 | Header |
| 1 | Header 'X' | 'X' = 0x58 | Header |
| 2 | Length | Do not exceed 0x7F | Number of bytes between LENGTH and CHECKSUM |
|  |  |  | Start counting LENGTH and contribute to CHECKSUM below this line |
| 3 | Attribute ID | 0x80 \| \(Attribute & 0x7F\) | LSB's of attribute |
| 4 | Attribute ID | \(Attribute & 0x3F80\) &gt;&gt; 7 | MSB's of attribute |
| 5 | Options | 0x42 | Reserved, set to 0x42 for API communications \(sets to absolute-write mode which can be used for polling telemetry too\) |
| 6 | TRID | 0x0 | Reserved transmit request ID |
| 7 | RRID | 0x0 | Reserved reply request ID |
| 8 - N | Payload | Payload contents |  |
|  |  |  | Stop counting LENGTH and stop contributing to CHECKSUM now |
| N+1 | Checksum | 255 - \(SUM\(Checksum-bytes\) % 256\) | Message verification checksum |

## Motor Drive QX Messages <a id="API-MotorDriveQXMessages"></a>

For each message ID, the bytes in the payload are shown as well as the code you would use to generate the message using the QX protocol provided by Freefly.

UC As UC, US As US, and UL As UL are 8, 16, and 32 bit unsigned binary values transmitted on the wire. FL As FL is a 32-bit floating point number transmitted in raw binary following standard C floating point conventions. 

### RPM Command \(Attribute ID 1010\): <a id="API-RPMCommand(AttributeID1010):"></a>

This command is only applicable if the drive is in speed-mode. In all other modes this command will be ignored.

| Payload Offset | Contents/Description | Length \(bytes\) | Type |
| :--- | :--- | :--- | :--- |
| 0 | Motor Identifier \(set to 0\) | 1 | UC As UC |
| 1-4 | RPM Command | 4 | FL As FL |

Example QX code:

```text
byte temp_byte = 0;
PARSE_UC_AS_UC(&temp_byte, 1, 0, 0); //Motor identifier
PARSE_FL_AS_FL(&rpm_command_float, 1, MAX_COMMAND_POSSIBLE, MIN_COMMAND_POSSIBLE); //Speed command
```

### Torque Command \(Attribute ID 1011\): <a id="API-TorqueCommand(AttributeID1011):"></a>

This command is only applicable if the drive is in torque-mode. In all other modes this command will be ignored.

This command follows the same structure as the RPM command, except the RPM command is replaced by a torque command \(in amps\).

**Angle Command \(Attribute ID 1012\):**

This command is only applicable if the drive is in angle-mode. In all other modes this command will be ignored.

This command follows the same structure as the RPM command, except the RPM command is replaced by an angle command \(in degrees support decimal precision\).

### Telemetry Packet 1 \(Attribute ID 1000\): <a id="API-TelemetryPacket1(AttributeID1000):"></a>

This packet can be polled at any time over QX regardless of what control or output mode the device is set in. It provides basic real-time monitoring potential for logging or displaying to the user on a dashboard.

When sending this message, you can optionally send dummy contents for all the data. The values will be ignored. You can also just send one byte. The only one that actually matters for polling is the motor identifier \(which should be set to 0\). The remaining bytes are ignored by the drive and need not be present. The response from the drive includes the telemetry in these fields.

| Payload Offset | Contents/Description | Units | Length \(bytes\) | Type |
| :--- | :--- | :--- | :--- | :--- |
| 0 | Motor Identifier \(set to 0\) |  | 1 | UC As UC |
| 1-4 | DC Voltage | Volts | 4 | FL As FL |
| 5-8 | DC Current \(sensor not present on all drive models\) | Amps | 4 | FL As FL |
| 9-12 | Phase A Current | Amps | 4 | FL As FL |
| 13-16 | Phase B Current | Amps | 4 | FL As FL |
| 17-20 | Phase C Current | Amps | 4 | FL As FL |
| 21-24 | Phase A Flux | Wb | 4 | FL As FL |
| 25-28 | Phase B Flux | Wb | 4 | FL As FL |
| 29-32 | Phase C Flux | Wb | 4 | FL As FL |
| 33 | Reserved, Ignore |  | 1 | UC As UC |
| 34 | Reserved, Ignore |  | 1 | UC As UC |
| 35 | Reserved, Ignore |  | 1 | UC As UC |
| 36-39 | Throttle Input Raw \(As telemetry, not command\) | N/A | 4 | FL As FL |
| 40-43 | DC Current, Estimated | Amps | 4 | FL As FL |
| 44 | Reserved, Ignore |  | 1 | UC As UC |
| 45 | Reserved, Ignore |  | 1 | UC As UC |
| 46 | ESC Fault State |  | 1 | UC As UC |
| 47 | ESC Soft Fault State |  | 1 | UC As UC |
| 48-41 | Brake Input Raw \(As telemetry, not command\) | N/A | 4 | FL As FL |

Example QX code:

```text
byte temp_byte = 0;
PARSE_UC_AS_UC(&temp_byte, 1, 0, 0); //Motor identifier
PARSE_FL_AS_FL(&vdc_v, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&idc_a, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&ia_a, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&ib_a, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&ic_a, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&flux_a, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&flux_b, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&flux_c, 1, FLT_MAX, -FLT_MAX);
byte ignore;
PARSE_UC_AS_UC(&ignore, 1, 0, 0);
PARSE_UC_AS_UC(&ignore, 1, 0, 0);
PARSE_UC_AS_UC(&ignore, 1, 0, 0);
PARSE_FL_AS_FL(&throttle_input_raw, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&idc_estimated_a, 1, FLT_MAX, -FLT_MAX);
PARSE_UC_AS_UC(&ignore, 1, 0, 0);
PARSE_UC_AS_UC(&ignore, 1, 0, 0);
PARSE_UC_AS_UC(&esc_fault_state, 1, 0xFF, 0);
PARSE_UC_AS_UC(&esc_soft_fault_state, 1, 0xFF, 0);
PARSE_FL_AS_FL(&brake_input_raw, 1, FLT_MAX, -FLT_MAX);
```

### Telemetry Packet 2 \(Attribute ID 1001\): <a id="API-TelemetryPacket2(AttributeID1001):"></a>

Follows the same concepts as Telemetry Packet 1.

| Payload Offset | Contents/Description | Units | Length \(bytes\) | Type |
| :--- | :--- | :--- | :--- | :--- |
| 0 | Motor Identifier \(set to 0\) |  | 1 | UC As UC |
| 1-4 | Q-Axis Current Command | Amps | 4 | FL As FL |
| 5-8 | Q-Axis Current Measured | Amps | 4 | FL As FL |
| 9-12 | D-Axis Current Command | Amps | 4 | FL As FL |
| 13-16 | D-Axis Current Measured | Amps | 4 | FL As FL |
| 17-20 | RPM Measured | RPM | 4 | FL As FL |
| 21-24 | PWM Out Magnitude | LSB's | 4 | FL As FL |
| 25-28 | Phase \(Voltage to BEMF Offset\) | Degrees | 4 | FL As FL |
| 29-32 | BEMF Absolute Angle | Degrees | 4 | FL As FL |
| 33-36 | Drive Temperature | Deg C | 4 | FL As FL |
| 37-40 | Q-Axis Integrator Loop Output | Volts | 4 | FL As FL |
| 41-44 | D-Axis Integrator Loop Output | Volts | 4 | FL As FL |
| 45-48 | Sensored Shaft Angle | Degrees | 4 | FL As FL |

Example QX code:

```text
byte temp_byte = 0;
PARSE_UC_AS_UC(&temp_byte, 1, 0, 0); //Motor identifier
PARSE_FL_AS_FL(&iq_command, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&iq_measured, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&id_command, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&id_measured, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&rpm_measured, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&pwm_out_mag, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&phase_offset, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&bemf_angle, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&temp_c, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&integrator_output_i_q, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&integrator_output_i_d, 1, FLT_MAX, -FLT_MAX);
PARSE_FL_AS_FL(&sensored_shaft_angle, 1, FLT_MAX, -FLT_MAX);
```

