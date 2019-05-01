# Motor Alignment

ALTA Pro’s motors are aligned at the factory at an angle relative to the chassis. This slight angle improves aircraft yaw authority and reduces the possibility of clockwise and counterclockwise turning motors from spinning at different speeds during stable hover. However, this alignment can be lost when opening the ALTA Pro chassis or if a boom needs to be replaced.

If the motors need to be realigned, follow the realignment procedure, then verify realignment was successful using the [Pixhawk Flight Review](https://goo.gl/DzmG1A) software.

To perform a realignment, Freefly recommends using a small, digital angle gauge with a flat surface so it can rest on the bottom of the motor mount \(for example, the Wixey WR300 angle gauge\).

### **Alta Pro Motor Realignment Procedure**

1. Place ALTA Pro on a level surface.
2. Place a digital angle gauge on the chassis next to the boom facing outwards.

![](https://lh6.googleusercontent.com/NhYsA_2f3_JGIBzzeDeXK6Jl051Tb29w7NW0mvQoZcr7R9S03ZN0Tt329F4uwNIl7PqQ9n3BjSGIMPI910HL3gqOsgsEvDvU4sx8Wv0sILUOWDlP2F-cNw2ZpGqlssHy4s3IQMwO)

3. Zero the angle gauge.  
4. Starting at motor 1, place the digital angle gauge on the flat surface of the motor mount  with the gauge facing outwards.

![](https://lh4.googleusercontent.com/WTAX7_XLlAlpoYmUqAJY1QUYXeZWi1YHE48z4PQCwyWD9cqpH0UKKCFKJPnhR_DE-7kuXc8lmuoabKcH8BafLSVATw_Io-GF6hYuVOzwoKHLZ_dybo0GipoBWUxjJU5zIMtpkv0G)

4**.** If the gauge reads a value outside the range 2.5°±0.1°, loosen the motor mount clamping bolts. While placing slight inward pressure on the motor, rotate the motor until the angle gauge indicates 2.5°±0.1°. When viewed from the end of the boom:

    a. Motors 1, 3, 5 and 7 should be rotated clockwise.



![](https://lh3.googleusercontent.com/F2ruG-Z3Ivy1X8oRlDtmngOiO62_sMNzMJkcqJiBRUg-gYlkwTWps4lScngKRLdmxBghw39-ELb0XqF3P_NJuaoqnD8mSpPLQMJmyuJmSzVJXwQOdn8wDdGnYAoVXGM2eCYZXIfv)

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **When rotating the motor, do not pull outwards on it.** |
| :--- | :--- |


6. Apply threadlock as required \(Loctite 222 recommended\), and tighten the motor mount bolts to 0.8 N-m \(7 in-lbs\). Do not over-torque the bolts.  
7. Repeat steps 2 through 6 for the additional motors.  
8. After aligning motors, recheck motor mount alignment and clamping bolt tightness.

## **Motor Alignment Verification Flight Test Procedure**

1. Complete Unpacking and Setup, Before Starting and Before Takeoff checklists.
2. Enter a hover for at least 10 seconds. Do not yaw during the hover.
3. Perform the ‘After Every Flight’ checklist.
4. Retrieve the microSD card from the GPS module and open it with a computer.
5. Open the ALTA Flight Data Viewer.
6. Drag and drop the latest .csv data log file of the test flight from the microSD card on to the ALTA Flight Data Viewer window.
7. Under the Data Seeker section, select Hover from the Seek Event drop down box.
8. In the Flight Statistics section, look at the Yaw CW Bias value. It should be within +/- 5%. It Yaw CW Bias is outside +/- 5%, recheck motor alignment.

| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **If the** [**Pixhawk Flight Review**](https://goo.gl/DzmG1A) **is unavailable or cannot be used on your operating system, yaw bias can be found at the bottom of the .csv data log for that flight.** |
| :--- | :--- |


