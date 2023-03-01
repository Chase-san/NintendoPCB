# DMG-GDAN-10

This board is a repair board based on the DMG-GDAN-10. The DMG-GDAN is used by F-1 Race, Kirby's Pinball Land, and Ultra Golf.

Unlike the other memory controllers, the MBC2 has ram onboard, preventing the need for an additional RAM chip. This board was mainly used by games that needed saves, but not much additional ram.

The original featured cut holes that were used for debugging or reference purposes, these have been omitted.

This board was designed to closely replicate the footprints and routes used by the original cartridge board.


## Components

This board features a 32-pin ROM. Like many boards before the MBC-3 this one features components that can be both axial/radial or SMD.

| Ref   | Package     | Description  | Notes | 
| :---: | :---------: | :----------- | :---- |
| U1    | SOP-32      | Program ROM  | |
| U2    | SOIC-28W    | MBC-2        | |
| U3    | SOIC-28     | System Reset | |
| C1    | Axial & 0603 | 10nF ±10% Capacitor | Only populate one |
| C2    | Axial & 0603 | 10nF ±10% Capacitor | Only populate one |
| C3    | Radial & 0603 | | Usually empty |
| R1    | Axial & 0603 | 10K Ohm 5% Resistor | Only populate one |

## Change Log

### R1 (2023-02-02)
- Initial build

## Images
![Front](https://github.com/Chase-san/NintendoPCB/blob/main/DMG-GDAN/images/front.png)
![Rear](https://github.com/Chase-san/NintendoPCB/blob/main/DMG-GDAN/images/back.png)

