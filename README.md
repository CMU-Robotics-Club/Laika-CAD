# Laika-CAD
 Quadruped Project CAD Repo

## 1: Description
This repo contains all the CAD for the CMU Robotics Club Quadrupeds Project. All CAD files, whether for the robot itself, a prototype, test structures, unused designs, or anything else should live within this repo. The CAD software of choice is SOLIDWORKS; non-SOLIDWORKS files should ideally be converted when possible or clearly marked with their respective software if conversion is problematic. The overall structure follows National Robotics Engineering Center EPDM standards as detailed below.

## 2: File Locations
The top level of CAD should only contain file folders and the top-level full assembly. Folders are created for submodules (legs, drivetrain, chassis, etc.) and for component types. COTS (Commercial Off-The-Shelf) components should be identified in a COTS folder; if generic enough to have application in multiple submodules, they should live in top-level COTS. The top-level COTS includes subdirectories for component types (fasteners, bearings, etc.). If a subdirectory appropriate for a part does not exist, create one. Note that these subdirectories should have more within them (for example, a FASTENERS subdir should contain BOLTS, NUTS and NUTS should contain NYLOC, PEM, JAM) If the COTS component is highly specific, should exist in lower level COTS folder in submodule directory. Files should generally be separated by file classifiers (see below). Top-level submodule directories should only contain 900-level files and 200-level files that belong to no subassembly. 200-level files which are part of subassemblies should be organized into descriptive subdirectories. All other file levels should be organized into subdirectories within the submodule directory (e.g. a simulation for a drive train motor shaft should be within a SIMULATION folder placed in the same directory as the top-level assembly for the drive train submodule). 000, 100, 400 series files should live within MANUFACTURING, DRAWINGS, and SIMULATION folders respectively placed within the same directory as the subassembly to which the relevant parts belong to.

## 3: File Naming
### 3.1: Custom
Custom parts should obey the XXXX YZZ - NAME file number convention:  
XXX: Module ID (Alphabetical)
Y: File type classifier (Numbers)
ZZ: Part number (Numbers)
NAME: Descriptive file name in Title Capitalization Form  

Example:
CYC 208 - Gearbox Mount Plate

The Module ID is an up-to-four-character code that describes the module the file belongs to. Should be as descriptive as four characters allow. The list of current module classifiers can be seen below:  
LAIK: Top-level assembly  
CHAS: Chassis  
DRIV: Drive train  
CYC: Cycloidal gearbox  
LEG: Leg design  
MTST: Motor test rig  
LTST: Leg test rig  

Please maintain this list as the project scope evolves.

The file type classifiers are as follows:  
0: Manufacturing file formats (STL, DXF, GCODE, etc.)  
1: Drawings  
2: Individual parts  
3: Equation .txt files  
4: Solidworks FEA Simulation Files  
5: Whatever weird stuff idfk
6: Weldments  
7: Piping, tubing, wiring, related  
8: Subassemblies  
9: Top-level assemblies. Typically no more than one (plus configurations) per module  

Please update this list as the scale of the project evolves.  

Part numbers should be defined beginning at 01. Number parts as they are created regardless of complexity, dependency, etc. Ensure that each part number for a given file type is only used once per subassembly. If you have more than 99 parts in a subassembly, you are doing something wrong!

Example:  
The completed drive train assembly would be named DRIV-901 - Drive Train Assem and would exist in the top-level DRIVE TRAIN folder.  
The housing subassembly would be DRIV-801 - Drive Train Housing and would exist in the lower-level DRIVE TRAIN/HOUSING folder.  
The drawing for one of the housing components would be DRIV-105 - Drive Train Top Cover and would exist in the DRIVE TRAIN/DRAWINGS folder.

### 3.2: COTS
COTS (Commercial Off-The-Shelf) parts should be named descriptively but do not need original part numbers. McMaster parts can be left as named when exporting as SLDPRT. Non-McMaster parts should be named descriptively, typically including part type, key dimensions, material as appropriate, etc. Additionally, should include manufacturer and part number. Use your best judgement! Someone with no project experience should be able to, from the file name, tell what the part is and where to order it.

### 3.3: Directories

Directories should be named in ALL CAPS. They should be named to describe the subassembly, component type, etc. 
