# The Surface Accelerations Reference - A Large-scale, Interactive Catalog of Passenger Vehicle Accelerations

## Introduction

The Surface Accelerations Reference is a catalog of all longitudinal and lateral accelerations experienced by SHRP2-NDS participants.
The Strategic Highway Research Program Naturalistic Driving Study (SHRP2-NDS) is the largest naturalistic driving study in the world constituting of 34.5 million miles of recorded driving data. To create the surface accelerations reference, each and every acceleration event in SHRP2-NDS was detected, summarized, and recorded creating a database of more than 1.7 billion data points. These data points were condensed to create a driving profile for each participant with signature kinematic measures within each roadway classification. The plots on the tool page compare such signature measures of SHRP2-NDS participants. 



## Methodology

Figure 1 shows the data flow diagram for the accelerations reference. Timeseries data from the SHRP2 NDS was first augmented with roadway attributes using HERE.com digital map data through in house map matching algorithms. This augmented timeseries data was then analyzed using the acceleration summarization algorithm illustrated in Figure 2.

</br>
<figure>
<img src="Accelerations_Reference_Data_Flow.svg" alt="drawing" class="center" style="display: block;  margin-left: auto;  margin-right: auto;  width: 80%;" />
<figcaption>Figure 1 - Data flow diagram for the accelerations reference.</figcaption>
</figure>
</br>

The acceleration summarization algorithm extracts, summarizes, and logs each acceleration event into the acceleration summary table. This is an intermediate table between the timeseries between the raw timeseries data and the final driver profiles.
</br>
<figure>
<img src="Breaking_Speed_and_Accel_WO_OUTLINE.svg" alt="drawing" class="center" style="display: block;  margin-left: auto;  margin-right: auto;  width: 100%;" />
<figcaption>Figure 2 - Extracting accelerations and decelerations periods from IMU and speed timeseries data.</figcaption>
</figure>
</br>
The driver profile generation process aggregates all the acceleration events and creates an individual profile for each driver with the measures for percentiles, rates, and strongest acceleration events in unit distance. These acceleration profiles form the back end dataset of this interactive analysis tool. The selections on the tool are processed to subset the dataset and generate the appropriate visualizations.



