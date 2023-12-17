Results are labeled as follows:
	1. Results [number] [descriptions] refers to the results gathered without using a Surprised based learning (SBL) algorithm, these are here for comparison and test
	and series of parameters such as rewards used, or type of surprise 
	2. P[Number] refers to the results gathered when using the unmodified SBL algorithm, with P refering to the pc value which
	controls volatility, the number represents the Pc value used
	3. RP[Number] is structured the same way as P[Number], but the RP shows those results with the SBL algorithm modified to choose
	actions randomly for the early parts of their runs

Within all of these folders results are broken down further:
	1. First their are the scenarios, denoting the different scenarios for the RDMSim
	2. Next their are the different runs, numbering 5 for each scenario

Lastly within the runs are the various results:
	Counts.txt contains various counts which refer to things such as topology selection and satisfaction amount/percentage
	FullTransitionProbs.txt and TransitionProbs.txt contain the transition probabilities at each timestep (the former contains ALL
	trantions probabilities, the latter only the one currently changed)
	ObservationProbs.txt contains the observation probabilities for each run
	InitialBelief.txt contains the beliefs at the start of each timestep
	RegressionResultsSolvePOMDP.txt files contain the parameters for a given quality attribute (QA), the belief in failure
	for this QA, and if the QA is satisifed
	SelectedAction&State.txt contains the selected action and state at each timestep

The Graphs folder is structured identically with two key differences:
	1. After picking the specific parameter folder (e.g. P06) there are 3 folders corresponding to different types of graphs:
		Graph 0 contains topology selections during runtime
		Graph 1 gives the average satisfaction of each QA, as well as the overall satisfaction
		Graph 2 contains the confidence intervals for each QA showing how far they are from being unsatisfied
	2. instead of the inner most folder containing the results it contains some graphical summary depending on the type of graph
	

