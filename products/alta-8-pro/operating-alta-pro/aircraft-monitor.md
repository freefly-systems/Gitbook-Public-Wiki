# Aircraft Monitor

ALTA Pro QGroundControl includes a flight status monitor that displays information about the health of the ALTA Pro and the various controls that can be selected.



| **Icon** | **Name** | **Description** |
| :--- | :--- | :--- |
| ![](https://lh4.googleusercontent.com/bCY4GAK1s2DAPEj7pHlFXo8urOymC4Fvr2otoC892z7SpR3d2npiuax69CygzJc49hvtGAMz2p414RGvxmeXhusD9wi8KgZ5MZnLFaVhdY3QgyWDeCdj5NVoCNl_HPn4VAeWAqG5) | Boot | Indicates if the PX4 has completed its booting process and whether it was successful. Any issues that prevented a normal boot are indicated here. |
| ![](https://lh6.googleusercontent.com/pg1NBUOURIp_3zju_cF3aIQ1dSKzU4spy5nFY_yHIGmA1XRKd9yThEhjP45dp7XpEGxXimdvVWcG1Xb65mX0yLe1m1oqweS7HJSlwc4R9OJ2N3QANL8Y3eFr5oZt_5nhLTERDAoo) | Battery | Displays the voltage of the battery packs. |
| ![](https://lh4.googleusercontent.com/Slql40KtcLl0z-J6sABDUFzFaqJQ2qHE8MF7eZmACsOvmLBYsPtCx-FkUpIqBjK_Z9JVqVQhy1yIK4bzkxO19Yfx79wKBd_2PszoiakoLou6kVgQswT91OozP7jGFLgRmGY3eSxB) | Status | Displays the state of the PX4 flight controller. |
| ![](https://lh6.googleusercontent.com/zSsjy-h8psdNVbtrbpP5EyELeJbtfeY6FP_L87DS7JII9Wm8UaFcSglTfM86QyME-DP7PUxncJ3Fze5_J8ejlCBXM9uZV_9S0ddPzMaNwe3csIWbHjigZz-2t0Ww5hDCZRC6ynWf) | Radio | Displays if the PX4 detects a radio controller signal. A LOS warning is displayed if no signal is present. |
| ![](https://lh3.googleusercontent.com/Gt2vTEBS1-tdSP-jtupbP0W6cMKMxSRQDNMP-9gD3LsryCDqwgNW6e0msgShyA0ftOyb-Qch9uhHyCAGkKNWwYPpdtBsHdiGm6YIUEIwO8ekxo6pZ_JfsLiwL7cdrf4ueneCB32w) | GPS  | Displays if PX4 has resolved a GPS fix or not. |
| ![](https://lh3.googleusercontent.com/Gt2vTEBS1-tdSP-jtupbP0W6cMKMxSRQDNMP-9gD3LsryCDqwgNW6e0msgShyA0ftOyb-Qch9uhHyCAGkKNWwYPpdtBsHdiGm6YIUEIwO8ekxo6pZ_JfsLiwL7cdrf4ueneCB32w) | Sats | Displays the number of GPS satellites in view and being received. A minimum of 6 satellites are required in order to enter Position Mode. |
| ![](https://lh3.googleusercontent.com/Gt2vTEBS1-tdSP-jtupbP0W6cMKMxSRQDNMP-9gD3LsryCDqwgNW6e0msgShyA0ftOyb-Qch9uhHyCAGkKNWwYPpdtBsHdiGm6YIUEIwO8ekxo6pZ_JfsLiwL7cdrf4ueneCB32w) | Lock | Clicking on this icon displays whether a position lock is ready, indicating a valid GPS fix and good heading. This is required before the Autopilot will allow switching into Position Mode. |
| ![](https://lh6.googleusercontent.com/jE_oTnGHxPymsb1zwT_TcY6OVT3D5kkwY-DQqFeKyQzvIuYepwVR_eyE9XB5zsduQkx0T-fz6GnDsyPXBtXYyqLqC1K5Oqtqg5YqUxp6qZTDXeWJM-dJLP22CHZRzjKfmteyN4xO) | Altitude | Displays the current height control mode: Manual, Vario if in Height or Position mode and climbing or descending, and Hold. |
| ![](https://lh6.googleusercontent.com/jE_oTnGHxPymsb1zwT_TcY6OVT3D5kkwY-DQqFeKyQzvIuYepwVR_eyE9XB5zsduQkx0T-fz6GnDsyPXBtXYyqLqC1K5Oqtqg5YqUxp6qZTDXeWJM-dJLP22CHZRzjKfmteyN4xO) | Attitude | Displays the current attitude control mode. |
| ![](https://lh6.googleusercontent.com/jE_oTnGHxPymsb1zwT_TcY6OVT3D5kkwY-DQqFeKyQzvIuYepwVR_eyE9XB5zsduQkx0T-fz6GnDsyPXBtXYyqLqC1K5Oqtqg5YqUxp6qZTDXeWJM-dJLP22CHZRzjKfmteyN4xO) | Compass | Displays the status of the compass and if the Autopilot believes the compass readings are good or bad. If Bad, the compass may require recalibration \(see the Compass Calibration section in this manual\). |
| ![](https://lh6.googleusercontent.com/jE_oTnGHxPymsb1zwT_TcY6OVT3D5kkwY-DQqFeKyQzvIuYepwVR_eyE9XB5zsduQkx0T-fz6GnDsyPXBtXYyqLqC1K5Oqtqg5YqUxp6qZTDXeWJM-dJLP22CHZRzjKfmteyN4xO) | Speed | Displays ground speed. |
| ![](https://lh6.googleusercontent.com/jE_oTnGHxPymsb1zwT_TcY6OVT3D5kkwY-DQqFeKyQzvIuYepwVR_eyE9XB5zsduQkx0T-fz6GnDsyPXBtXYyqLqC1K5Oqtqg5YqUxp6qZTDXeWJM-dJLP22CHZRzjKfmteyN4xO) | Flight Time | Displays the amount to time the aircraft has been flying**.** |

