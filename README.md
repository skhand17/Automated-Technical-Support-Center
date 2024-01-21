Technical Support Center Modeling and Simulation
Overview
This project contains code to model and simulate the operations of a technical support center to analyze metrics like turnaround time, escalation rate, and resolution time of each of three engineering teams namely: TechnicalSupportEngineer, EscalationEngineer, and PremiumSupportEngineer.

The code also provides with the turnaround time and throughput of the entire support center for hundreds of customers cases.

Contents
The project contains the following:
•	Simulation engine code in Java that handles discrete event simulation logic.
•	It contains the following Java files:
CustomerCase.java
CustomerCaseGenerator.java
TechnicalSupportCenter.java
TechnicalSupportEngineer.java
EscalationEngineer.java
PremiumSupportEngineer.java
Transducer.java
Running Simulations
To run a simulation:
1.	Please create a package name called Component.Project under Models directory in DEVS-Suite
2.	Copy all these java files under this package name.
3.	Launch the sim launcher.
4.	Under Configure File System, Add the package Component.Project.
5.	Select this package and select model TechnicalSupportCenter.
6.	Click on Simview and Tracking followed by next.
7.	A coupled model named TechnicalSupportCenter will open.
8.	Orange component is a CustomerCaseGenerator.
9.	Light Blue component is SupportCenterRouter.
10.	 Green color component is Level I TSE.
11.	 Pink color component is Level II EE.
12.	 Light gray color component is Level III PSE.
13.	 Light Pink color component is TransducerPerformanceAnalyzer.
14.	 Right click on start on the coupled model and run step for 20 to 30 iterations step by step.
15.	 One could see different combinations of customer cases are being generated and different combinations could be viewed.
a.	Case is routed to TSE and resolved by TSE. On resolving the case, it appends the solution to the customer case model.
b.	Case is routed to TSE but then escalated to EE and EE resolves the case, in such situation the EE resolves the case and sends the solution as feedback to the level I.
c.	Case is routed to EE but then EE escalates the case to PSE. The PSE resolves the case and sends feedback to the EE. EE updates its internal database and sends the same solution with case notes back to TSE. TSE updates its internal database.
16.	After running few manual iterations to see the behavior, run step for 1000 or 2000 time to see the end results produced by the Transducer.
17.	Try changing the observation times, processing times for each level to see different behavior, observations, and metrics.
Documentation
Full documentation on the model methodology, configuration parameters, analysis examples, and modules can be found in the Project Report.
Contributing
Contributions and extensions to the model are welcome through pull requests. The code will be uploaded to GitHub soon.

