https://github.com/user-attachments/assets/145927b7-b68a-468a-8b0a-571980a8af83

# PMW3389 Custom DIY Mouse

A fully custom gaming mouse using an Arduino Pro Micro ATmega32U4 and a PixArt PMW3389.

I also intend for this mouse to be easily repairable.

## Key Features

- High performance sensor: 16,000DPI via PixArt PMW3389
- Modular and Repairable
	- Hotswap Main Switches: Uses Mill-Max 3305 so can be replaced with no soldering
	- Replacable MCU: Mounted with Through-Hole Header
- Communication through SPI bus

## How To Use

1. Order PCB from PCB manufacturer (e.g. JLCPCB)
2. Either get PCBA or hand solder components
3. Download Library. Instructions in [Library](Firmware/README.md)
4. Download [Firmware](Firmware/examples/BasicMouse/BasicMouse.ino)
5. Flash firmware.

## Components

- Sensor: PixArt PMW3389 and LM19-LCT Lens

- MCU: 3.3V Pro Micro (ATmega32U4)

- Switches: 2 x Huano Blue Shell Pink Dot Mouse Switches 

- Controls: Rotary Encoder w/Switch (EC11)

- Hot Swap Socket for Switches: 6 x Mill-Max 3305

- SMD stuff (0805)
	- 1 x 13 ohm resistor
	- 1 x 10k ohm resistor
	- 5 x 0.1uF capacitor
	- 3 x 10uF capacitor
	- 1 x 4.7uF capacitor
	- 1 x XC6206P182MR 65K5 LDO

- PTFE Mouse Skates

- Micro USB Cable

## Pinout

- PMW3389
	- NCS -> D10
	- MOSI -> D16 (MOSI)
	- MISO -> D14 (MISO)
	- SCLK -> D15 (SCLK)
	- MOT -> D2 (INT 1)

- Rotary Encoder w/Switch
	- A -> D3 (INT 0) (SCL) (internal pullup)
	- B -> D7 (INT 6) (internal pullup)
	- S2 (Used for Switch) -> D8

- Switches
	- Switch 1 -> D4
	- Switch 2 -> D9

## Documentation & Credits

- [Build & Design Log](CHANGELOG.md)
- [Third-Party Credits & Libraries](CREDITS.md)
- [MIT License](LICENSE)
