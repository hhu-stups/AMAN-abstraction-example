## How to reproduce the results from the paper:


### Inspecting the machine files 
* The whole folder is a Rodin project. Check it out!

### Reproducing the State Space Visualisation 
* First start ProB2-Ui (https://www3.hhu.de/stups/downloads/prob/tcltk/nightly/)
* Load the .prob2project file
* Select the Machine MAbs (Abstraction)
* Go to the verification reiter on the right
* Select the (+) and click on "Model check" wait till the checking finishes
* Go to "Visualisation" reiter on the top left, there got to "Graph Visualization" in the opening window go to "State Space projection expression."
* Select "Example1"; ProB2 should now calculate and load the visualization

### Reproducing the Traces 
* For Machine MAbs the trace described in the paper can be found in the left corner ("example2"); a click on it replays it.
* Machine MAbs_helper contains the refined trace.
* To redo the trace refinement, go to MAbs_helper, and select the recycle button on the bottom left. 
* Choose "Refine Trace" in the drop-down menü
* As origin set MAbs
* As target set MAbs_helper
* Check the box at the bottom.
* Press "start"

### Model checking 
* The model checking was run on Linux and a nightly version of ProBCLi
* Example Command (insert your own path to probcli)
  ```Downloads/ProB/probcli --model-check -p OPERATION_REUSE full -pref_group model_check unlimited -p COMPRESSION TRUE -noass -memory -p TIME_OUT 5000 -p MAX_OPERATIONS 100000 -p MAX_INITIALISATIONS 100000 <FileName> ```
* MAbs and M9 were checked this way
