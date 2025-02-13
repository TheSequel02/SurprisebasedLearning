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

### The Graphs folder is structured as follows:
1. All graphs are stored in the graphs folder
2. Within the graphs folder are several more folder which indicate the parameters
 1. Results [number] [descriptions], for example Results 3 (Flat transition), refers to the results gathered without using a Surprised based learning (SBL) algorithms.
 2. P[Number], for example P0655, refers to the results gathered when using the unmodified SBL algorithm, with P refering to the pc value which controls volatility, the number represents the Pc value used. Thus P0655 refers to a instance of our SBL where the PC value is set to 0.655
 3. RP[Number] is structured the same way as P[Number], but the RP shows those results with the SBL algorithm modified to choose actions randomly for the early parts of their runs. So RP06 has a PC value of 0.6, but the first 50 timesteps chooses action randomly.
 
3. Within a specific parameters folder (such as P0636) are 3 more sub-folders, each corresponding to a specific type of graph:
	1. Graph 0 contains topology selections during runtime
 	2. Graph 1 gives the average satisfaction of each QA, as well as the overall satisfaction
  	3. Graph 2 contains the confidence intervals for each QA showing how far they are from being unsatisfied
4. Lastly, within each graphs folder are more sub folders corresponding to a given scenario, and then graphs corresponding to a specific run
	. It should be noted that depending on the type of graph there may be an extra graph at the same point in the folder structure as the scenarios which will contain information about all runs for that scenario, summarized based on averages

# Graphs contents
As stated there are 3 types of graphs, here is a more detailed breakdown of what each contains:
1. Graph 0 is a bar chart which describes how often each of our two topologies was chosen throughout a run, with the y axis giving the total count (titled "occurance rate") and x axis labelling which topology is being described
2. Graph 1 is similar to graph 0 but references how often a given QA was satisified over a run, the y axis giving the percentage of that run that the NFR was satisfied, the x axis labelling which NFR the value corresponds to (avg giving the average of all three NFR's)
3. Graph 2 is a confidence plot of our monitorable variables, and shows us how far the variables are from being satisifed/unsatisfied. Unlike the other graphs the runs are not seperated into different files, instead within each scenario is an image corresponding to each monitorable variable. The y-axis labels what run is being represented, the x axis will be value for the monitorable variable, the dots give the average value of the variable for a run, and the tails next to the dot give a confidence interval that value may also fall into. Lastly the red line indicates the acceptable threshold, for MC and MP the values of the variable should be below the redline to be satisifed and for MR the values should be above the red line.

	
