# Visual-Delimitation-Survey-Design-Models
Probabilistic models used to evaluate a novel visual survey design methodology based on transect data and scouting, for three case studies

The associated files were created for the following proposed manuscript: A novel design method for customized visual delimiting surveys for plant pests based on transects and scouting. We propose using transects customized for the pest species and situation to collect data on at least 60 detections, fit the distance data to an exponential function, estimate a percentile boundary distance, and use field scouting for verification. We call this approach “Delimitation via Transect Data and Scouting”, or DTDS. 

We identified published delimitation survey plans or results of activities for three species, all of which have host plants. Using available information, we created customized DTDS plans for each species, and then compared the sampling effort required to complete the original and novel plans, for localized populations. We used simulations in five of the case studies to compare the results under uncertainty and to evaluate outcomes when mapped spatially.

Simulation specifications

Overview. Models were built to emulate the survey conditions (e.g., areas, host densities, infestation rates) and survey plan specifications (areas and hosts inspected). Outputs were number of infected/infested hosts detected, by plan or scenario. We also estimated the inspection time required per host and the total time taken, again by plan or scenario.

Functions and parameters. Because of the number of models and survey plans created for evaluations, we cannot exhaustively present the functions or parameters used. Parameters came from the source or were standardized: only survey specifications differed in simulations, not situational details. For parameters with a single, mean estimate (e.g., trees per km2), in every case we added uncertainty by using lower and upper values that were ten percent different from the mean, and used a uniform distribution to sample values (i.e., every value equally likely). For example, if authors estimated 10,000 hosts per km2, the lower limit was 9,000 and the upper limit was 11,000.

Nearly all functions used were basic arithmetic, such as calculating infestation densities (no. per unit area), area sizes (e.g., π × R2), or widths. One exception was the binomial process. In this process, n independent, identical trials are run, each one with the same probability of success, p, producing some number of successes, s (Vose 2000):

s = RiskBinomial(N, p) [11]

This function was used, for example, to find the number of infested cells or hosts detected, where N was the number inspected and p was the infestation rate. We assumed perfect detection (i.e., sensitivity = 1.0) for simplicity.

General specifications. The models were all coded in spreadsheets and run using @Risk ver. 7.5.1 Professional Edition (Palisade Corporation, 31 Decker Road, Newfield, NY 14867), a Microsoft Excel add-in. Unless otherwise specified below, simulation settings were as follows: number of iterations = 100,000; sampling type = Latin Hypercube; and random seed = 101.
