# Tuning ALTA Pro's Flight Controller

ALTA Pro’s Flight Controller comes pre-tuned for a wide variety of payloads and flying conditions. Generally, additional tuning is not required to fly ALTA Pro, and will only need to take place if more customization of control feel is desired. Default tuning values are included in Appendix A, Default Tuning Values.

| ![](https://lh6.googleusercontent.com/ugslLYofjq1aeJzjU0a4QIb1mo4ga9KcBmv4LhwJBurfFlqTDKkA9UkgJ7tf8Ztibwl5EpcNijrKIMgEkIWe18lajvUm7zumPxPiApD84d5ebpLIStSDIJkbXoOKJiyVLR1f2yGF) | **DO NOT CHANGE FLIGHT CONTROLLER TUNING VALUES WITHOUT A FULL UNDERSTANDING OF THE TUNING PROCESS. A poorly tuned sUAV is dangerous and can result in property damage, injury, and death.** |
| :--- | :--- |


Parameters fall into three categories: Rate, Attitude, and Position. Typically, tuning should take place in that order, ensuring Rate parameters are set first, then moving to Attitude parameters, and finally Position parameters.

Before tuning, users should read and become familiar with the [PX4 Tuning Guide](https://docs.px4.io/en/config_mc/pid_tuning_guide_multicopter.html#rate-controller).To tune ALTA Pro, open the ALTA Pro QGroundControl connect to your ALTA Pro and navigate to the Multicopter Attitude Control and Multicopter Position Control parameters groups under the Parameter Tab in the Vehicle Setup menu. Once you have found the parameter pages follow the instructions in the [PX4 Tuning Guide](https://docs.px4.io/en/config_mc/pid_tuning_guide_multicopter.html#rate-controller).

![](https://lh5.googleusercontent.com/Um9sBTl-QfvYRagWuS3iiGtLa5tI-r1Xh7KgG1f53edIIlMqbb-rTkQ2Z-4suQkA_7nF0TFyt5EFt7sXDr-EMDvvLAEIZU1MOjNr-yLHmzDRIsS2L-_2DJCti2hErl_TdQqKNXfU)



| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **Tuning can change the fundamental flying characteristics of ALTA Pro. It is possible for ALTA Pro to become unstable or even uncontrollable if values are set too high or too low. Only change tuning parameters in small increments and with caution. Always test new tuning configurations in open areas away from people or obstacles.** |
| :--- | :--- |


| ![](https://lh5.googleusercontent.com/b0z4o4yMxQeV8z7I93ZpTlSyAqQ8XrOX5VQDOAqn73iMA2rnqSYP3F9VGliP2WRyBe7YIPrcSGWCiI6XWf_2dScGHGFLyxo4paycq71ktk9cF6MCxo_W6aUdihv6oQkKrMsMJHQc) | **While ALTA Pro QGroundControl allows users to tune their ALTA Pro in the air we suggest changing tuning values while ALTA Pro is on the ground as a precautionary measure.** |
| :--- | :--- |


| ![](https://lh4.googleusercontent.com/HpkEwm74tCXUHVxImUfvCUkE04-iQ-h21xWSkmyaEQP5CzrLm4OysE2cnVw0DON3CuMoEmrgzff2GmjRm21o-IwCWSyTs0Ucol0e7o1yR2o_okWGSGOJ2iEpgutZiLaMSubR7i6c) | **When making configuration changes with ALTA Pro QGroundControl, make sure to save each parameter as you change them!** |
| :--- | :--- |


## \*\*\*\*

