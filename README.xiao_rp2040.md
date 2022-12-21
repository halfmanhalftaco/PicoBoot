PicoBoot for Seeed Studio Xiao RP2040 board
===========================================

This modifies the pin assignments from the [original repository](https://github.com/webhdx/PicoBoot) to work
on the [Seeed Studio Xiao RP2040 board](https://www.seeedstudio.com/XIAO-RP2040-v1-0-p-5026.html).

Build the firmware same as described in [README.md](README.md), put Xiao into bootloader mode by holding down the 'B" button while plugging in, drop `picoboot.uf2` file into the virtual drive. Like on the original PicoBoot, disconnect the 3V3 line from your GameCube while uploading/updating firmware.

Referring to the original [Wiring Diagram](./assets/Wiring%20diagram.jpg), this is how pins map from Pico to the Xiao [(pinout here)](./assets/xinpin.jpg):


| Pico   | Xiao   | Function |
|--------|--------|----------|
| GP4    | P1     | CS       |
| GP5    | P2     | CLK      |
| GP6&7  | P26&27 | DATA     |

GND and 3V3 should be fairly obvious.

Keep in mind that the original author explicitly does not support non-Pi Pico boards, so use this at your own risk. 
I take no responsibility for bricking your Gamecube or frying your Xiao.
