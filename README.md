### Results are labeled as follows:
1. Results [number] [descriptions], for example Results 3 (Flat transition), refers to the results gathered without using a Surprised based learning (SBL) algorithm, these are here for comparison and test and series of parameters such as rewards used, or type of surprise. To go back to the example Results 3 just refers to the order it was collected, (Flat transition) is the important distinguisher, this one specifically means the results were gathered using transition probabilities that are all set to equal one another.
2. P[Number], for example P0655, refers to the results gathered when using the unmodified SBL algorithm, with P refering to the pc value which controls volatility, the number represents the Pc value used. Thus P0655 refers to a instance of our SBL where the PC value is set to 0.655
3. RP[Number] is structured the same way as P[Number], but the RP shows those results with the SBL algorithm modified to choose actions randomly for the early parts of their runs. So RP06 has a PC value of 0.6, but the first 50 timesteps chooses action randomly.

### Within all of these folders results are broken down further:
1. First their are the scenarios, denoting the different scenarios for the RDMSim
2. Next their are the different runs, numbering 5 for each scenario.

### Lastly within the runs are the various results:
* Counts.txt attempts to summarize some key metrics present in the data, such as how often topology is selected or how satisified each quality attribute (QA) is. These values will be given as both a raw count and as a percentage of the run.
* FullTransitionProbs.txt and TransitionProbs.txt are deprectated and currently should not contain anything
* ObservationProbs.txt contains the observation probabilities for each run at each timestep
* InitialBelief.txt contains the beliefs at the start of each timestep
* RegressionResultsSolvePOMDP.txt files contain the parameters for a given QA, the belief in failure for this QA, and if the QA is satisifed
* SelectedAction&State.txt contains the selected action and state at each timestep

### The Graphs folder is structured identically with two key differences:
1. After picking the specific parameter folder (e.g. P06) there are 3 folders corresponding to different types of graphs:
	1. Graph 0 contains topology selections during runtime
 	2. Graph 1 gives the average satisfaction of each QA, as well as the overall satisfaction
  	3. Graph 2 contains the confidence intervals for each QA showing how far they are from being unsatisfied
2. instead of the inner most folder containing the results it contains some graphical summary depending on the type of graph
	
