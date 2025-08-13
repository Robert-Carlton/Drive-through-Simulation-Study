# Summary
This study examined how a busy restaurant’s drive-thru operations could be improved to reduce traffic hazards caused by long vehicle queues spilling onto nearby roads. The restaurant, located near a major intersection, frequently experienced congestion during peak hours, raising the risk of accidents and increasing emissions from idling cars. Using video-based data collection and the ARENA simulation platform, I modeled customer flow through order, payment, and pickup stations.

Several data collection methods were tested, including manual timing, automated computer vision tracking, and hybrid approaches, with manual tracking ultimately used to develop accurate arrival rate estimates. These arrival rates were validated against exponential distributions using statistical goodness-of-fit tests. The simulation tested how changes in staffing affected queue lengths and roadway encroachment.

Results showed that small, targeted staffing increases could dramatically reduce both wait times and the number of incidents where queues extended into the street. For example, adding just half an extra staff member during peak periods reduced roadway-impacting queues by over 95%. With three or more staff, the risk of roadway encroachment was nearly eliminated. The findings suggest that low-cost staffing adjustments, rather than expensive facility redesigns, can significantly improve safety and efficiency.

The methodology used in this study—combining real-world observational data, statistical validation of arrival patterns, and simulation modeling—can be applied to a wide range of scenarios beyond restaurant drive-thrus. Similar techniques could help optimize traffic flow at toll booths, ferry terminals, or event venue entrances where queuing can create safety hazards. They could also be used in logistics hubs, airport security lines, or border crossings to evaluate operational changes before implementation. By pairing accurate data collection with simulation, operators can test low-cost interventions—such as staffing adjustments, lane reconfiguration, or process sequencing—without disrupting real-world operations, leading to safer, more efficient systems.

# Highlights

:heavy_check_mark: Problem: Long drive-thru queues at a busy intersection caused traffic hazards, potential accidents, and increased emissions.

:heavy_check_mark: Goal: Use simulation to evaluate low-cost operational changes that prevent queues from spilling into roadways.

:heavy_check_mark: Data Collection

  * Used synchronized video feeds from webcams to track vehicles through order, payment, and pickup points.
  * Tried automated tracking with CV2, PyTorch, YOLO5, and SORT, but faced challenges with vehicle identification in curved lanes.
  * Settled on manual timing to estimate arrival rates (λ) for each station.

:heavy_check_mark: Analysis

  * Generated synthetic exponential arrival data from observed rates.
  * Validated these distributions using Kolmogorov-Smirnov and Anderson-Darling tests, confirming good fits.
  
:heavy_check_mark: Simulation

  * Built in ARENA with logic for customers choosing the shortest order lane.
  * Added visual alerts when queues exceeded lot capacity.
  * Tested scenarios with varying staffing levels.

:heavy_check_mark: Results

  * Baseline (2 staff): ~136 roadway queue incidents; avg. wait 12.9 minutes.
  * +0.5 staff: ~6 incidents; avg. wait 3.6 minutes.
  * 3 staff: <1 incident; avg. wait 2.5 minutes.
  * 3.5 staff: virtually eliminated roadway queues (0 incidents in simulation).

:heavy_check_mark: Conclusions

  * Real-world video analytics for this purpose is challenging but promising.
  * Small staffing changes can significantly improve safety and customer experience.
  * Future enhancements could include modeling traffic light impacts or refining in-restaurant workflow.
