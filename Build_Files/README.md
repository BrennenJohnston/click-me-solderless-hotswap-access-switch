# Build files

This folder contains the build files for the device.

- `PCB_Build_Files/`: everything uploaded to the board manufacturer: the Gerber
  ZIP, the parts list (`BOM_ClickMe.csv`) and the component placement file
  (`CPL_ClickMe.csv`). See `Documentation/ORDERING.md`.
- `3D_Printing_Files/STL/`: the four housing parts and the five keycap options.
  Print `Part_0` to `Part_3` and exactly one `Part_4.x`. See
  `Documentation/ASSEMBLY.md`.

The STL files are saved in assembly position rather than laid out for printing,
so load them into a slicer one at a time or drop each one onto the build plate.
