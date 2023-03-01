# NintendoPCB

This repository is for the reproduction and documentation of various Nintendo PCBs. Specifically targeting the Gameboy series of handheld consoles.

# License

These boards are released under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. See the LICENSE for more details.

In short, don't sell these designs or boards produced from these designs, and do attribute the designs to me.

# Gameboy GamePak PCB Designs

At present these are designed as repair boards for the official Nintendo Gameboy games. The intention is for the components from the original pcb to be transplanted directly to these boards. However a list of parts is made available if these are not otherwise available. These boards are designed to closely replicate the original tracks and fill zones of the original. These do NOT have the intention of fooling others into thinking they are official boards.

These are NOT designed to be used for Flash Carts, but rather to repair official games.
Please see HDR's [MBC3-Flashcart](https://github.com/HDR/MBC3-Flashcart) and [MBC30-Flashcart](https://github.com/HDR/MBC30-Flashcart) for PCB designs useful as flashcarts.

## Nintendo Board ID

Nintendo uses roughly the following system for producing the ID for a board.

`SYSTEM-ID-REVISION`

`SYSTEM` is either DMG or more rarely GBC, referring to the original Gameboy or the Gameboy Color.

`ID` is the actual ID of the board.

`REVISION` is the revision of the board. Most boards only have a single revision in the wild, but others, such as the DMG-BEAN have up to 6. Every revision I have seen has been electronically compatible with minor track, via, or fill differences.

## Differences from Official PCB

Each of these may have several revisions by Nintendo, I will usually try to base my board off the latest revision where possible. Despite this there are significant differences in design in a few regards compared to official PCBS.

### Debug Tracks and Holes

The Official PCBs make use of tracks which are interconnected, but which are then drilled out. I am unsure of the exact purpose of these, but they were likely for grounding purposes during manufacturing. Most of these have been removed as they serve no purposes for the repair board.
While it is possible that these extra tracks may allow special RF interactions, this does not appear to be by design.

### Thermal Relief

The Official PCBs make use of a different thermal relief pattern than KiCAD. Replicating the factory thermal relief pattern is possible but time consuming. Therefore these are often changed to the method KiCAD uses. Additionally some components may have had thermal relief added where it may be reasonable to do so.

### Identifying Marks

Some of these have been removed or altered.

- The revision number has been changed from a two digit number to "R#" where # is the repair board revision.
- The text "Repair Board" has been added near the board identifier.
- My initials and the year and month of the design have been added.
- Some non-informative identifying marks have been removed. Such as the large numbers on the front of the boards and the circle markers for the date identifier boxes.

### Tracks and Fill

While I make an effort to closely replicate the original board, some features may not be identical to the original. Some features are non-trivial to replicate and therefore an approximation has been used instead.

The main example of this being the battery fill which is fully circular on the repair boards.

## Ordering / Using the Gerber Files

I highly recommend using a service such as [JLCPCB](https://jlcpcb.com/) to get these manufactured. The following are the options that should be selected.

- Layers: 2
- Dimensions: 51mm x 60.7mm / 2" x 2.39"
- PCB Thickness: 0.8mm / 0.0315" (required)
- Surface Finish: ENIG or Hard Gold (required)
- Gold Fingers: Yes (required)
- Finger Chamfer: 45° (recommended)
- Copper Weight: 1 oz or higher (recommended)
- Color: Green (suggested), other colors have longer lead times

Of note, Hard Gold is very expensive so ENIG is a good option. The thicker the layer of gold the better the longer the pins will last. A heavier copper weight is nice but not required.

## Board List

These are the boards. Please check your original for the required one. Only boards with a revision number have a repair board developed.

Each folder related to this project is a distinct KiCAD project, containing subfolders with images of the repair board and scans of the original board it was based on.

This list is NOT exhaustive.

| Revision | ID       | MBC    | ROM      | RAM      | Battery | Other        |
| :------: | :------- | :----: | :----:   | :------: | :-----: | :----------- |
|          | CGB-A32  | MBC-6  | SOP-32   | SOP-28   | CR1616  | Flash        |
| [R3](https://github.com/Chase-san/NintendoPCB/releases/tag/dmg-a02-r3) | DMG-A02  | MBC-5  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-A03  | MBC-5  | TSOP2-44 | SOP-28   | CR1616  |              |
|          | DMG-A04  | MBC-5  | TSOP-32  | SOP-28   | CR1616  | Rumble       |
|          | DMG-A06  | MBC-5  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-A07  | MBC-5  | SOP-32   | N/A      | N/A     |              |
|          | DMG-A08  | MBC-5  | TSOP2-44 | SOP-28   | CR1616  |              |
|          | DMG-A09  | MBC-5  | TSOP2-44 | N/A      | N/A     |              |
|          | DMG-A11  | MBC-5  | TSOP2-44 | SOP-28   | CR1616  | Rumble       |
|          | DMG-A14  | MBC-5  | TSOP2-44 | SOP-28   | CR2025  |              |
|          | DMG-A15  | MBC-5  | TSOP2-44 | SOP-28   | CR2025  | 2x ROM       |
|          | DMG-A16  | MBC-5  | SOP-32   | SOP-32   | CR2025  |              |
|          | DMG-A40  | MBC-7  | SOP-32   | N/A      | N/A     | Tilt/EEPROM  |
|          | DMG-A47  | MBC-7  | TSOP2-44 | N/A      | N/A     | Tilt/EEPROM  |
| [R1](https://github.com/Chase-san/NintendoPCB/releases/tag/dmg-aaa-r1) | DMG-AAA  | N/A    | MQFP-44  | N/A      | N/A     |              |
|          | DMG-BBA  | MBC-1  | SOIC-24  | N/A      | N/A     |              |
|          | DMG-BEAN | MBC-1  | SOP-32   | N/A      | N/A     |              |
|          | DMG-BFAN | MBC-1  | SOP-32   | N/A      | N/A     |              |
|          | DMG-DECN | MBC-1  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-DEDN | MBC-1  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-DGCU | MBC-1  | TSOP2-44 | SOP-28   | CR1616  |              |
| [R1](https://github.com/Chase-san/NintendoPCB/releases/tag/dmg-gdan-r1) | DMG-GDAN | MBC-2  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-KECN | MBC-3  | SOP-32   | SOP-28   | CR2025  | Clock        |
|          | DMG-KFCN | MBC-3  | SOP-32   | SOP-28   | CR2025  | Clock        |
|          | DMG-KFDN | MBC-3  | SOP-32   | SOP-28   | CR2025  | Clock        |
| [R4](https://github.com/Chase-san/NintendoPCB/releases/tag/dmg-kgdu-r4) | DMG-KGDU | MBC-3  | TSOP2-44 | SOP-28   | CR2025  | Clock        |
|          | DMG-LFDN | MBC-3  | SOP-32   | SOP-28   | CR2025  | Clock        |
|          | DMG-MHEU | MBC-30 | TSOP2-44 | SOP-28   | CR2025  | Clock        |
|          | DMG-TEDN | HuC-1  | SOP-32   | SOP-28   | CR1616  | IR           |
|          | DMG-TFDN | HuC-1  | SOP-32   | SOP-28   | CR1616  | IR           |
|          | DMG-UEDT | HuC-3  | TSOP1-32 | TSOP1-28 | CR2025  | IR/Clock     |
|          | DMG-UFDT | HuC-3  | TSOP1-32 | TSOP1-28 | CR2025  | IR/Clock     |
|          | DMG-UGDU | HuC-3  | TSOP2-44 | TSOP1-28 | CR2025  | IR/Clock     |
|          | DMG-Z02  | MBC-5  | SOP-32   | SOP-28   | CR1616  |              |
|          | DMG-Z03  | MBC-5  | TSOP2-44 | SOP-28   | CR1616  |              |
|          | DMG-Z04  | MBC-5  | TSOP2-44 | SOP-28   | CR1616  | Rumble       |

# Game Usage

Here is a list of the primary games using the given boards. Some boards have a lot of games or the game that uses the board is not particularly popular. Some games have used multiple boards (mostly pokemon).

| ID        | Main Usage  |
| :-------  | :---------  |
| CGB-A32   | Net de Get - Minigame @ 100 (Japan) |
| DMG-A02   | Pokemon Red/Blue, Lots of other games. |
| DMG-A03   | Wario Land 2/3 |
| DMG-A04   | Pokemon Pinball |
| DMG-A06   | Game & Watch, Mega Man Xtreme 2 |
| DMG-A07   |  |
| DMG-A08   | TLOZ: Oracle of Ages/Seasons  |
| DMG-A09   | Rayman, Tony Hawk Pro Skater 2 |
| DMG-A11   | Pokemon Pinball  |
| DMG-A14   |  |
| DMG-A15   |  |
| DMG-A16   |  |
| DMG-A40   | Kirby Tilt & Tumble  |
| DMG-A47   |  |
| DMG-AAA   | Catrap, Dr. Mario, Tetris  |
| DMG-BBA   |  |
| DMG-BEAN  | Mega Man II-V, Pacman |
| DMG-BFAN  | Mortal Kombat I/II |
| DMG-DECN  | Donkey Kong, Donkey Kong Land, Super Mario Land 2  |
| DMG-DEDN  | Pocket Monsters Aka, Midori (Japan) |
| DMG-DGCU  | Dragon Quest Monsters  |
| DMG-GDAN  | Kirby's Pinball Land |
| DMG-KECN  | Bokujou Monogatari GB  |
| DMG-KFCN  | Mary Kate & Ashley Pocket Planner |
| DMG-KFDN  | Pokemon Gold/Silver/Crystal  |
| DMG-KGDU  | Pokemon Gold/Silver/Crystal  |
| DMG-LFDN  | Pocket Monsters Pikachu (Japan) |
| DMG-MHEU  | Pokemon Crystal (Japan)  |
| DMG-TEDN  | Pocket Bomber Man (Japan) |
| DMG-TFDN  | Pokemon Card GB (Japan) |
| DMG-UEDT  | Pocket Family GB  |
| DMG-UFDT  | Pocket Family GB  |
| DMG-UGDU  | Pocket Family GB 2  |
| DMG-Z02   | Mega Man Xtreme |
| DMG-Z03   |  |
| DMG-Z04   | Pokemon Pinball  |
