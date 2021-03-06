# TII-2017

This is the code associated to the article: 

V. Rodríguez-Fernández, A. Gonzalez-Pardo, and D. Camacho, “Automatic Procedure Following Evaluation using Petri Net-based Workflows,” IEEE Trans. Ind. Informatics, vol. In press, 2017.

You can find a link to the article here:
[TBD]

## Requirements

1. Download and install Oracle Java 8.
2. Download and install Netbeans IDE.
3. Open the project using Netbeans IDE.

## Usage

There are several run configurations attached to this Netbeans project:

### Run configuration TII (main file: examples/TIIExperimentation.java)

This the main run configuration associated to the article. In a nutshell, it reads a datalog from a xlsx file,
loads the WF-Net-based OP "Engine Bay Overheating", and applies the APFE algorithm.

Two arguments are used in this run cofiguration. You can edit them in Project Properties->Run.

1. Path of the datalog: The data log must be a .xlsx file with 3 columns (See the article):
* x (timestamp)
* v (varname)
* R(x,v) record of v at time x

An example of a datalog file can be found at `resources/datalogs/STANAG_4586_log_formatted.xlsx`

2. Path of the JSON file containing the information of the OP to use. See an example of this information file in
`resources/OPInfo/TII_ENGINE_BAY_OVERHEATING.json`

### Run configuration GUI

This is the main file inherited from the PetriNet Simulator [PetriNetSim](https://github.com/zamzam/PetriNetSim). 
Click the "Open" button and select the file `resources/WFNetOP/TII_EBO.pnml` to load the WF-Net-based OP used in the 
article. 

Select a transition, right click on it and go to the tab "APFE" in order to see how the guard condition associated to 
that transition is implemented.

## Contact

For any questions about the use of the code or the creation of new WF-Net based Operating Procedures, please contact me by email or add a new issue in this repository.
