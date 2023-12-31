# ARCADE XML Generator

## Pip install instructions
```
pip install arcade-xml-generator==0.0.1
```
## Running instructions
To run the arcade_xml_generator run ```gui.py``` in your preferred python interpreter. From there, simply select the values you wish to simulate and then hit run-- it's that simple. 
When the module is fully released, interactions with this gui will create a setup .xml file for use with ARCADE.

## Background on ARCADE
ARCADE is an agent-based modelling system, created by the Bagheri lab, that is provides information on emergent properties of groups of cells. ARCADE runs in java but requires .xml files to provide the rules to its agents. The parameter options are stored in separate .xml files and interfacing between the two can be challenging. 
### Versions
Arcade is a flexible software that allows for different setups depending on the module. This allows for simulations of different tissues such as wound healing or tumor growth. Two notable ARCADE modules are Patch and Potts. Currently the xml_generator is only set up for patch but planned development includes a potts module. 
### Structure of Set Up .xml File
The set up .xml file that is produced by the ARCADE XML Generator will have the following primary branches:
* Series and Set -- These parameters general instructions for the simulation such as how long the simulation is, the tick rate, and how many simulations should be run. 
* Populations -- These parameters determine the rules for the agents such as tumor cells or healthy tissue cells.
* Actions -- These parameters determine disturbances to the population such as mutations or injury.
* Layers -- These parameters determine the environment such as oxygen or TGFA.
* Components -- These parameters determine the spatial organization of the layers. 
  An example of this file can be seen in docs/example_output/setup_hex.xml
These files are produced by parsing multiple .xml files and combining them with user input. A patch setup file, for instance, reads in both a parameter.xml file and parameter.patch.xml file.


## Dependencies
The primary dependencies of this software are PyQt, ElementTree, sys, os, dataclasses, typing, and copy.

## To be Developed
### Coming in this Version
* Ability to save GUI inputs
* Compiling functionality
* Patch functionality

### Future Versions
* Linter
* Run Commands in Bash
* Run directly into ARCADE button
* Potts functionality
