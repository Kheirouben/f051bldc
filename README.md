# f051bldc
The goal of this project is to create a brushless firmware for the stm32 mcu's. The firmware is intended to work on a number of vehicle types.
The project file can be opened in Atollic truestudio, there is also an attached cubemx file showing the peripheral setup.
The firmware is currently working well for ground vehicles but high performance quadcopter usage is still under development. For now max erpm is about 250k until further testing is done.

What works:
Dshot 1200.
ProShot 1000.
Servo Pwm.

Dshotcommands to change direction, enable 3d mode and save settings to eeprom.
(through betaflight cli)

"dshotprog 255 10" enables bi-dir mode.
"dshotprog 255 12" saves settings.

3d mode or bididrectional for vehicle modes.
Drag brake and adjustable brake strength in vehicle mode.
Complemenetary pwm, freewheeling.

Vehicle mode 1 ( quad mode ) uses eeprom for settings. 

Vehicle mode 2 ( crawler mode) comp_pwm and max braking, instant reverse.

Vehicle mode 3 ( car mode ) uses adjustable strength brake on first reverse and requires double tap to change direction.

Vehicle mode 4 ( car mode but will reverse itself when motor has slowed )
