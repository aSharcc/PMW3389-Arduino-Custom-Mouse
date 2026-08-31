https://github.com/user-attachments/assets/145927b7-b68a-468a-8b0a-571980a8af83

# PMW3389 Custom DIY Mouse

A fully custom gaming mouse using an Arduino Pro Micro ATmega32U4 and a PixArt PMW3389.

I also intend for this mouse to be easily repairable.

Be sure to read [BOM.md](docs\BOM.md)

## Key Features

- High performance sensor: 16,000 DPI via PixArt PMW3389
- Modular and Repairable
	- Hotswap Main Switches: Uses Mill-Max 3305 so can be replaced with no soldering
	- Replaceable MCU: Mounted using through-hole pin headers
- Sensor communication through SPI

## How To Use

**DETAILED INSTRUCTIONS and BOM [HERE](docs/BOM.md)**

1. Order the PCB from a PCB manufacturer (e.g. JLCPCB). [Files](https://github.com/aSharcc/PMW3389-Arduino-Custom-Mouse/releases/tag/2.0)
2. Either:
   - Order PCBA for the SMD components, or
   - Purchase the SMD components and hand solder them.
3. Purchase the components listed in the BOM that are not included in PCBA.
4. Hand solder/install the components not included in PCBA.
5. Download the PMW3389 library. See [Library](Firmware/README.md) for instructions.
6. Download [Firmware](Firmware/examples/BasicMouse/BasicMouse.ino).
7. Flash the firmware to the Pro Micro.
8. Download and print the 3D models from [STL Files](Mechanical/v2/STLs).
9. Add threaded heat inserts to the shells.
10. Assemble the mouse.

## Components

- Sensor: PixArt PMW3389 and LM19-LCT Lens

- MCU: 3.3V/8MHz Pro Micro (ATmega32U4)

- Switches: 2 x Huano Blue Shell Pink Dot Mouse Switches 

- Scroll Wheel: Rotary Encoder w/Switch (EC11)

- Hot Swap Socket for Switches: 6 x Mill-Max 3305

- SMD Components (0805)
	- 1 x 13 ohm resistor
	- 1 x 10k ohm resistor
	- 5 x 0.1uF capacitor
	- 3 x 10uF capacitor
	- 1 x 4.7uF capacitor
	- 1 x XC6206-1.8V LDO

- PTFE Mouse Skates

- Micro USB Cable

- Mounting Hardware
	- 7 x Heat Insterts M2 x 3 x 3.2
	- 3 x M2 x 4 Screw
	- 4 x M2 x 7 Screw

## Pinout

- PMW3389
	- NCS -> D10
	- MOSI -> D16 (MOSI)
	- MISO -> D14 (MISO)
	- SCLK -> D15 (SCLK)
	- MOT -> D2 (INT 1)

- Rotary Encoder w/Switch
	- A -> D3 (INT 0) (internal pullup)
	- B -> D7 (INT 6) (internal pullup)
	- S2 (Used for Switch) -> D8

- Switches
	- Switch 1 -> D4
	- Switch 2 -> D9

## Documentation & Credits

- [Build & Design Log](CHANGELOG.md)
- [Third-Party Credits & Libraries](CREDITS.md)
- [MIT License](LICENSE)