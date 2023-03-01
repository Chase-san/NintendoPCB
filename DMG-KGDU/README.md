# DMG-KGDU

This board is a repair board based on the DMG-KGDU-10. The DMG-KGDU is used by the USA versions of Pokemon Gold, Silver, and Crystal.

The original featured cut holes that were used for debugging purposes, these have been omitted.

This board was designed to closely replicate the footprints and routes used by the original cartridge board. All components may be sourced from an original cart.

## Components

This board features a 44-pin ROM and a 28-pin RAM module.

| Ref   | Package     | Description  | Notes | 
| :---: | :---------: | :----------- | :---- |
| U1    | TSOP-II-44W | Program ROM  | ~10.1mm wide |
| U2    | LQFP-32     | MBC-3        | |
| U3    | SOIC-28W    | SRAM         | ~8.3mm wide |
| U4    | SOIC-8      | System Reset | ~4.3mm wide |
| C1,C2 | 0603 (in)   | 15pF Capacitor | |
| C3, C4, C5, C6 | 0603 (in) | 15nF Capacitor | Anything up to 0.1μF is supproted |
| R1    | 0603 (in)   | 1kOhm Resistor | |
| R2    | 0603 (in)   | 330kOhm Resistor | |
| X1    | 6mm x 2mm   | 32.768 kHZ Cystal | 12.5 pF Load and 35 kOhm ESR |

## Change Log

### R4 (2023-02-03)
- Fillet the tracks
- Fix teardrops
- Fix various pad connections.

### Rev3 (2023-01-29)
- Added teardrops to vias and pins. Should help in fabs with lower standards, they also look nicer.
- Modified the X1 no copper zone to better reflect the original boards.
- Rounded the corners of the X1 cutout to be easier to manufacture.
- Removed the last of the silk screen.

### Rev2 (2023-01-21)
- Board redesigned based on high resolution scans.

### Rev1 (2023-01-20)
- Initial build based on photos.

## Images
![Front](https://github.com/Chase-san/NintendoPCB/blob/main/DMG-KGDU/images/front.png)
![Rear](https://github.com/Chase-san/NintendoPCB/blob/main/DMG-KGDU/images/back.png)

