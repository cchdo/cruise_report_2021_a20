Total Alkalinity
================

PI
  * Andrew G. Dickson – SIO
  * Frank Millero - RSMAS
Technicians
  * Manuel Belmonte
  * Carmen Rodriguez

Total Alkalinity
----------------
The total alkalinity of a sea water sample is defined as the number of moles of hydrogen ion equivalent to the excess of proton acceptors (bases formed from weak acids with a dissociation constant K :math:`\leq` 10–4.5 at 25°C and zero ionic strength) over proton donors (acids with K > 10–4.5) in 1 kilogram of sample.

Total Alkalinity Measurement System
-----------------------------------
Samples are dispensed using a Sample Delivery System (SDS) consisting of a volumetric pipette, various relay valves, and two air pumps controlled by LabVIEW 2012. 
Before filling the jacketed cell with a new sample for analysis, the volumetric pipette is cleared of any residual from the previous sample with the aforementioned air pumps.
The pipette is then rinsed with new sample and filled, allowing for overflow and time for the sample temperature to equilibrate. 
The sample bottle temperature is measured using a DirecTemp thermistor probe inserted into the sample bottle and the volumetric pipette temperature is measured using a DirecTemp surface probe placed directly on the pipette.
These temperature measurements are used to convert the sample volume to mass for analysis.

Samples are analyzed using an open cell titration procedure using two 250 mL jacketed cells. 
One sample is undergoing titration while the second is being prepared and equilibrating to 20°C for analysis. 
After an initial aliquot of approximately 2.3-2.4 mL of standardized hydrochloric acid (~0.1M HCl in ~0.6M NaCl solution), the sample is stirred for 5 minutes while air is bubbled into it at a rate of 200 scc/m to remove any liberated carbon dioxide gas.
A Metrohm 876 Dosimat Plus is used for all standardized hydrochloric acid additions.
After equilibration, ~19 aliquots of 0.035 ml are added. 
Between the pH range of 3.5 to 3.0, the progress of the titration is monitored using a pH glass electrode/reference electrode cell, and the total alkalinity is computed from the titrant volume and e.m.f. measurements using a non-linear least-squares approach ([Dickson2007]_).
An Agilent 34970A Data Acquisition/Switch Unit with a 34901A multiplexer is used to read the voltage measurements from the electrode and monitor the temperatures from the sample, acid, and room. 
The calculations for this procedure are performed automatically using LabVIEW 2012. 

Sample Collection
-----------------
Samples for total alkalinity measurements were taken at all A20 Stations (1-90).
Three Niskin bottles at each station were sampled twice for duplicate measurements except for stations where 24 or less Niskin bottles were sampled.
Stations at which 24 or less Niskin bottles were sample one or two Niskin bottles were sampled twice for duplicate measurements. 
Using silicone tubing, the total alkalinity samples were drawn from Niskin bottles into 250 mL Pyrex bottles, making sure to rinse the bottles and Teflon sleeved glass stoppers at least twice before the final filling.
A headspace of approximately 3 mL was removed and 0.05 mL of saturated mercuric chloride solution was added to each sample for preservation.
After sampling was completed, each sample’s temperature was equilibrated to approximately 20°C using a Thermo Scientific Isotemp water bath.


Problems and Troubleshooting
----------------------------
On one occassion, during analysis of station 25, the Agilent 34901A Data Acquisition/Switch Unit shut off and did not power back on. The unit had to be replaced with a spare and sample analysis was not interrupted. 
Throughout the cruise, glitches from the Sample Delivery System were experienced at random. At one point, the laptop controlling the SDS powered off and would not return back on. This too was replaced with a spare. 
Additionally, the Sample Delivery System program would freeze drawing sample in Deliver Sample or Prepare Pipette mode and caused a few sample bottles 
to be emptied. This resulted in a few lost samples. Furthermore, due to a novice operator, during analysis of station 34 the Metrohm 876 Dosimat Plus calibration was changed and samples were run with the incorrect calibration. However,
the lead technician was able to find this error and corrected the mistake. Only 6 samples were analyzed using the icorrect dosimat calibration function but were recalculated to correct for this error. 


Quality Control
---------------
Dickson laboratory Certified Reference Material (CRM) Batch 178 and 180 were used to determine the accuracy of the total alkalinity analyses. The total alkalinity certified value for these batches are:

* Batch 187 2204.98 ± 0.37 µmol/kg (32;16)

* Batch 192 2213.70 ± 0.53 µmol/kg (32;16)

The cited uncertainties represent the standard deviation. 
Figures in parentheses are the number of analyses made (total number of analyses; number of separate bottles analyzed).

At least one reference material was analyzed at every A20 stations resulting in 142 reference material analyses. 
On A20, the measured total alkalinity value for each batch is:

* Batch 187 2205.54 ± 1.79 µmol kg-1 (107) [mean ± std. dev. (n)]

* Batch 192 2214.45 ± 1.58 µmol kg-1 (33) [mean ± std. dev. (n)]


If greater than 24 Niskin bottles were sampled at a station, three Niskin bottles on that station were sampled twice to conduct duplicate analyses.
If 24 or less Niskin bottles were sampled at a station, one or two Niskins on that station were sampled twice for duplicate analyses.
The standard deviation for the duplicates measured on A20 is:

Duplicate Standard Deviation ± 2.10 µmol kg–1 (111) [± std. dev. (n)]

The total alkalinity measurements for each A20 stations have been compared to measurements taken from the neighboring A20 2021 stations.

1689 total alkalinity values were submitted for A20. 
Further dilution corrections need to be applied to this data and will not be applied until onshore, therefore this data is to be considered premilinary.
