# Laika-CAD
 Quadruped Project CAD Repo

## 1: Description
This repo contains all the CAD for the CMU Robotics Club Quadrupeds Project. All CAD files, whether for the robot itself, a prototype, test structures, unused designs, or anything else should live within this repo. The CAD software of choice is SOLIDWORKS; non-SOLIDWORKS files should ideally be converted when possible or clearly marked with their respective software if conversion is problematic. The overall structure follows National Robotics Engineering Center EPDM standards as detailed below.

## 2: File Locations
The top level of CAD should only contain file folders. Folders are created for submodules (legs, drivetrain, chassis, etc.) and for component types. COTS (Commercial Off-The-Shelf) components should be identified in a COTS folder; if generic enough to have application in multiple submodules, they should live in top-level COTS. The top-level COTS includes subdirectories for component types (fasteners, bearings, etc.) If a subdirectory appropriate for a part does not exist, create one. Note that these subdirectories should have more within them (for example, a FASTNERS subdir should contain BOLTS, NUTS and NUTS should contain NYLOC, PEM, JAM) If the COTS component is highly specific, should exist in lower level COTS folder in submodule directory. Files should generally be separated by file classifiers (see below). Top-level submodule directories may only contain 900-level files and 200-level files should be organized into descriptive subdirectories. All other file levels should be organized into subdirectories within the submodule directory (e.g. a simulation for a drive train motor shaft should be within a SIMULATION folder placed in the same directory as the top-level assembly for the drive train submodule). 

## 3: File Naming
### 3.1: Custom
Custom parts should obey the XXX-YZZ file number convention:
XXX: Module ID
Y: File type classifier
ZZ: Part number

The Module ID is a three-character code that describes the module the file belongs to. Should be as descriptive as three characters allow. The list of current module classifiers can be seen below:
DOG: Top-level assembly
CHA: Chassis
DRV: Drive train
LEG: Leg design
TST: Test rig
Please maintain this list as the project scope evolves.

The file type classifiers are as follows:
0: Manufacturing file formats (STL, DXF, GCODE, etc.)
1: Drawings
2: Individual parts
3:
4: Solidworks FEA Simulation Files
5:
6: Weldments
7: Piping, tubing, wiring, related
8: 
9: Top-level assemblies. Typically no more than one (plus configurations) per project.
Please update this list as the scale of the project evolves.

Part numbers should be defined beginning at 01. Number parts as they are created regardless of complexity, dependency, etc. Ensure that each part number for a given file type is only used once per subassembly. If you have more than 99 parts in a subassembly, you are doing something wrong!

### 3.2: COTS
COTS (Commercial Off-The-Shelf) parts should be named descriptively but do not need original part numbers. McMaster parts can be left as named when exporting as SLDPRT. Non-McMaster parts should be named descriptively, typically including part type, key dimensions, material as appropriate, etc. Additionally, should include manufacturer and part number. Use your best judgement! Someone with no project experience should be able to, from the file name, tell what the part is and where to order it.

### 3.3: Directories

Directories should be named in ALL CAPS. They should be named to describe the subassembly, component type, etc. 
