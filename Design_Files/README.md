# Design files

This folder contains the design files for the device.

`PCB_Design_Files/` holds the circuit exported from EasyEDA Pro in several
interchange formats so it can be opened in most circuit design tools:

- `Altium_*.zip`, `PADS_*.zip`, `DISA_*.zip`: schematic and board in Altium,
  PADS and DISA formats.
- `PDF_*.zip`: the schematic as a PDF, for reading without any EDA tool.
- `Netlist_Schematic1_*.tel`: the netlist: three parts and two nets.
- `BOM_Board1_*.xlsx`, `PickAndPlace_*.xlsx`: the unmodified EasyEDA exports.
  The upload-ready versions in `Build_Files/PCB_Build_Files/` differ: they omit
  `U2`, the mechanical keyboard switch, which the maker supplies.

CAD source files for the printed parts are not published yet. They exist in
Fusion 360 and will be added once cleaned up.
