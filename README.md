<!--- Repository structure follows the Open Assistive Technology (OpenAT) Template by Makers Making Change --->

# Click Me: Solderless Hot-Swap Access Switch

A 3D-printed accessibility switch you build without soldering, where the button
itself is an ordinary mechanical keyboard switch you can swap in seconds to change
how hard it is to press.

- **Ordering guide**: `Documentation/ORDERING.md`
- **Assembly guide**: `Documentation/ASSEMBLY.md`
- **Bill of materials**: `Documentation/BOM.csv`
- **Assembly animation**: [youtu.be/RXbbdtwFPiI](https://youtu.be/RXbbdtwFPiI)
- **Status**: work in progress. Built and used, still being iterated

<img src="Photos/in-use-pressed-toy-running.jpg" width="640" alt="A black-gloved finger presses the large lime-green button of a Click Me switch, and the toy it is plugged into responds. A black cable runs from the switch to a toy fire truck with a red cab and a clear body full of red, blue and teal gears; the truck's lights are lit and teal beams shine from its side across the pale wood table.">

## Why this exists

Because I work in the assistive technology field, I end up needing a lot of access
switches, and the ones you can buy cost far more than they should for what is
really a button and a 3.5 mm jack. The part that bothers me more is that they
arrive with one actuation force baked in, so when a switch is too heavy or too
light for the person in front of me, there is not much I can do about it except
order a different switch and wait.

So this is my attempt at a switch where the button is a cheap mechanical keyboard
switch that pulls out and pushes back in by hand. If the force is wrong, you change
it in seconds for the price of a coffee, and hopefully the switch ends up fitting
the person instead of the other way round.

## What it does

- **Plugs into anything with a 3.5 mm switch jack**: switch-adapted toys,
  communication aids, switch interfaces
- **Needs no soldering**: the board arrives from JLCPCB with both parts fitted
- **Needs no screws or glue**: the printed housing snaps together
- **Lets you tune the press**: any Cherry MX compatible keyboard switch fits, in
  whatever force, feel, and sound suits the person
- **Comes with five keycaps**: different sizes and heights, one with a tactile
  pattern you can find by touch

Three of the five keycaps, each on a finished Click Me: flat and textured at the
back left, a tall flat-topped mound at the back right, and the one with the
tactile pattern in front.

<img src="Photos/keycap-options-printed.jpg" width="640" alt="Three finished Click Me switches on a wood table, each with a different keycap. Back left: a flat lime-green keycap with a finely textured top, in a black housing over a grey layer and a light blue base. Back right: a tall lime-green keycap whose sloped sides rise to a raised flat square, in a magenta housing over a grey layer and a light blue base. In front: an all-black Click Me with a tall red keycap shaped like a four-sided pyramid, with a raised, finely ridged X on its peak whose arms point to the corners.">

## What it costs

About **$8.43 per finished switch** at the moment: $4.82 for the assembled board,
$3.00 for the cable, $0.42 of filament, and $0.19 for the mechanical keyboard
switch. That is with everything bought in small volumes, which is the worst case.
A bigger batch of boards alone took the board cost from $4.82 down to $2.36.
Full breakdown from my own orders is in
[ORDERING.md](Documentation/ORDERING.md#8-what-it-costs).

The Click Me is open assistive technology (OpenAT). Under the terms of the
open-source licenses in this repository, the device may be built, used, and
improved upon by anyone.

## How to obtain the device

### 1. Do it yourself

Order the circuit board following [ORDERING.md](Documentation/ORDERING.md), print
the parts, and build it following [ASSEMBLY.md](Documentation/ASSEMBLY.md). You
need a 3D printer, or access to one.

### 2. Build it for someone else

The board has a minimum order quantity, so building one leaves you with spares.
Most of the board cost is charged once per order rather than per board, so a
bigger batch is much cheaper per unit; 50 boards cost me slightly less in total
than 25 did. That makes this a practical device for a lending library, a school,
or a program to build in quantity, as long as you prove a revision on a small
batch first. See
[ORDERING.md](Documentation/ORDERING.md#how-many-to-order).

## Build instructions

1. **Read [ORDERING.md](Documentation/ORDERING.md)** and order the circuit board
   from JLCPCB with assembly turned on. This is the long-lead item, so order it
   first and print while you wait.
2. **Buy a mechanical keyboard switch** and a 3.5 mm mono cable. Which keyboard
   switch to choose is covered in
   [ASSEMBLY.md section 3](Documentation/ASSEMBLY.md#3-choosing-your-mechanical-keyboard-switch).
3. **Print the four housing parts and one keycap** from
   [`Build_Files/3D_Printing_Files/STL/`](Build_Files/3D_Printing_Files/STL).
4. **Assemble it** following [ASSEMBLY.md](Documentation/ASSEMBLY.md). No
   soldering, no screws, no glue.

## Files

### Documentation

| Document | Link |
|---|---|
| Ordering guide | [ORDERING.md](Documentation/ORDERING.md) |
| Assembly guide | [ASSEMBLY.md](Documentation/ASSEMBLY.md) |
| Bill of materials | [BOM.csv](Documentation/BOM.csv) |
| Changelog | [CHANGES.txt](CHANGES.txt) |

### Build files

| What | Link |
|---|---|
| Gerber files, and the upload-ready ZIP | [`Build_Files/PCB_Build_Files/`](Build_Files/PCB_Build_Files) |
| JLCPCB parts list and placement files | [`BOM_ClickMe.csv`](Build_Files/PCB_Build_Files/BOM_ClickMe.csv), [`CPL_ClickMe.csv`](Build_Files/PCB_Build_Files/CPL_ClickMe.csv) |
| 3D printing files | [`Build_Files/3D_Printing_Files/STL/`](Build_Files/3D_Printing_Files/STL) |

### Design files

| What | Link |
|---|---|
| Circuit design exports and schematic | [`Design_Files/PCB_Design_Files/`](Design_Files/PCB_Design_Files) |

The circuit is exported from EasyEDA Pro in several interchange formats (Altium,
PADS, DISA) plus a schematic PDF and a netlist, so it can be opened in most
circuit design tools.

**CAD source files for the printed parts are not in this repository yet.** They
exist (the parts were designed in Fusion 360) and will be published once they
have been cleaned up. Until then the STL meshes are what is available, so the
printed parts can be reproduced but not easily modified.

### Photos

Assembly photographs, board close-ups and renderings are in
[`Photos/`](Photos). Every one of them is described in words in
[ASSEMBLY.md](Documentation/ASSEMBLY.md), so no step depends on being able to see
an image.

## The circuit

A momentary single-pole switch, and nothing else:

| Reference | Part | LCSC | Fitted by |
|---|---|---|---|
| CN1 | PJ-320B 3.5 mm mono jack | C22355831 | JLCPCB |
| U1 | CPG151101S11-16 hot-swap socket | C41430893 | JLCPCB |
| U2 | Mechanical keyboard switch | none | You, by hand |

The jack's tip and sleeve connect through the keyboard switch. The ring is
deliberately left unconnected, which is the standard assistive-technology switch
pinout: a mono plug works, and a stereo plug still makes contact on tip and
sleeve.

The board is 46 x 46 mm (1.81 x 1.81 in) with rounded corners, two layers, 1.6 mm FR-4.

`U2` appears in the circuit design so the switch footprint positions the housing
cutout correctly, but it is **not** in the files uploaded to JLCPCB, because the maker
supplies that part. See [ORDERING.md](Documentation/ORDERING.md) section 5.

## How to improve this device

This is an open prototype and improvements are welcome. Directions worth exploring:
a latching or toggle variant, a version with two switches on one base, mounting
points for a clamp or mounting arm, a keycap with a replaceable tactile symbol, and
CAD sources so the housing can be resized.

If you build one, the most useful feedback is which keyboard switch you chose and
how the actuation force suited the person using it.

## License

Copyright (c) 2026 Brennen Johnston.

This repository describes Open Hardware:

- Everything needed or used to design, make, test, or prepare the Click Me is
  licensed under the [CERN 2.0 Weakly Reciprocal license (CERN-OHL-W v2) or
  later](https://cern.ch/cern-ohl).
- All software is under the [GNU General Public License v3.0 or later
  (GPL-3.0-or-later)](https://www.gnu.org/licenses/gpl.html).
- Accompanying material such as instruction guides and photographs, which are
  useful but not necessary to design, make, test, or prepare the Click Me, is
  published under a [Creative Commons Attribution-ShareAlike 4.0 license
  (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

You may redistribute and modify this documentation and make products using it
under the terms of the [CERN-OHL-W v2](https://cern.ch/cern-ohl).
This documentation is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY,
INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR
PURPOSE. Please see the CERN-OHL-W v2 for applicable conditions.

License texts are in [`LICENSES/`](LICENSES).

Source Location: https://github.com/BrennenJohnston/click-me-solderless-hotswap-access-switch

## Attribution

The device was designed by Brennen Johnston.

The documentation and repository structure follow the OpenAT Template created by
Makers Making Change / Neil Squire Society, used under a CC BY-SA 4.0 license:
[github.com/makersmakingchange/OpenAT-Template](https://github.com/makersmakingchange/OpenAT-Template).

### Contributors

Designers:
- Brennen Johnston

Testers:
- Brennen Johnston
