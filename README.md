# USBtoN64v2
Utilizes STM32F446 on a Nucleo-F446RE with custom header or on a fully custom board for usb and n64 communication.

In this repository, you can find the latest version of the source code (TrueSTUDIO), 3D case (.stl), and PCB (Eagle .brd and .sch) files.

Currently supported USB devices:
- Keyboard
- Dualshock 3 Sixaxis
- Dualshock 4 (with help from Kazon Wilson [kwilson21])
- Wireless Xbox 360 with Microsoft USB wireless receiver
- Wired Xbox 360
- Wired Xbox One

## Setting the controls:
1) Press the blue button on the Nucleo or the only button on the custom PCB. A new green LED (light) should light up solid when you go into "set controls" mode, and it should turn off when you finish setting the controls correctly.
2) Press the buttons in the appropriate order depending on which device is plugged in. For Xbox and PS, you also need to set range and deadzone. Please see below for instructions.
3) (optional) Press the same button again at any time to exit “set controls” mode early if you make a mistake.

### Xbox / Playstation:
DPAD_UP, DPAD_DOWN, DPAD_LEFT, DPAD_RIGHT, BUTTON_START, BUTTON_B, BUTTON_A, C_UP, C_DOWN, C_LEFT, C_RIGHT, BUTTON_L, BUTTON_R, BUTTON_Z

Next you set your RANGE. It starts at 100 by default.
Up (+) and Down (-) on the D-pad will increase or decrease the range by 5.
Right (+) and Left (-) on the D-pad will increase or decrease the range by 1.
The range cannot be greater than 100 or less than 0.
When you are done, hit "A" on the Xbox controller or "X" on the Playstation controller to move on.

Next you set your DEADZONE. It starts at 20 by default.
Up (+) and Down (-) on the D-pad will increase or decrease the deadzone by 5.
Right (+) and Left (-) on the D-pad will increase or decrease the deadzone by 1.
The deadzone cannot be greater than 100 or less than 0.
When you are done, hit "A" on the Xbox controller or "X" on the Playstation controller. Congratulations, you are done configuring your controls!

### KB:
A_UP, A_DOWN, A_LEFT, A_RIGHT, DPAD_UP, DPAD_DOWN, DPAD_LEFT, DPAD_RIGHT, BUTTON_START, BUTTON_B, BUTTON_A, C_UP, C_DOWN, C_LEFT, C_RIGHT, BUTTON_L, BUTTON_R, BUTTON_Z

Note that the device saves the controls even when the device is powered off. It saves the Xbox and Playstation controls together as a shared layout and the Keyboard controls separately.

Currently known bugs
- None!

## TODO:
- Complete LED support for PS4 (currently non-functional)
- Re-design PCB (and case) to be significantly smaller (in progress)

By: Ownasaurus

## Special thanks to:
????? ????? [Rainshifter] for help and support along the whole process

Kazon Wilson [kwilson21] for help with Dualshock 4 support

???? ????? [Serisium] for help with PCB design and understanding the STM32 hardware

Jeff Longo [?????] for help with PCB design and 3D case design
