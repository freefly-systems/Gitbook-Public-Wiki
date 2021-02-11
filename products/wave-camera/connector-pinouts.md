# Connector Pinouts

## GPIO Connector

The GPIO connector provides two general-purpose inputs \(GPI\) and two general-purpose outputs \(GPO\). The figure below shows the pinout of this connector and the color coding of the Mōvi Pro Wave Remote Control Cable \(Freefly P/N 910-00661\).

![GPIO Connector Pinout and Color Coding](../../.gitbook/assets/image%20%287%29.png)

### Mōvi Pro Wave Remote Control Cable

The Mōvi Pro Wave Remote Control Cable \(Freefly P/N 910-00661\) is available on the [Freefly Store](https://store.freeflysystems.com/collections/wave/products/movi-pro-wave-remote-control-cable).  You can use this now for remote start/stop on your Mōvi Pro. It will also enable full camera control via UART in a future firmware update. You can also use this as a donor cable to wire up a custom remote start/stop for other systems \(see below\).

To configure the correct remote start/stop signal on the Mōvi Controller, the Camera Type should be set to ARRI RS in the FIZ Config menu.

### Custom Remote Start/Stop

A custom remote start/stop cable can be created by following the wiring diagram below. The GPIO are optically isolated, so the host must supply a voltage \(3.3V or 5V is okay\) to power its side of the optocoupler. The current drawn will be &lt;20mA.

![Wiring of a custom remote start/stop cable.](../../.gitbook/assets/image%20%2826%29.png)

The momentary switch connects the GPI2/RS pin to GND \(0V\). Each single press will toggle the recording state on or off, just like the dedicated Record Button. For wireless remote start/stop, a relay- or transistor-based RC switch can also be used.

