LADCP
=====

PI
  * Dr. Andreas Thurnherr

Data Acquisition and QC
-----------------------

In order to collect full-depth profiles of horizontal and vertical ocean velocity, two Acoustic Doppler Current Profilers (ADCPs), 
one facing upward (uplooker) and the other downward (downlooker), as well as a Deep Sea Power And Light 
rechargeable 48V battery and cables were installed on the CTD rosette.
This lowered ADCP (LADCP) system was provided by the Lamont-Doherty Earth Observatory.
The LADCP system is self contained, requiring on-deck cable connections to charge the battery and for communicating with the ADCPs.
The battery charger was affixed to an elevated cable run in the CTD bay and connected to a long power cord extension
terminating on a bench in the wet lab next to the bulkhead door leading to the CTD bay.
On the bench, the LADCP data acquisition computer, a Mac Mini, as well as two bench-top power supplies for the ADCPs were installed. 

Between casts the LADCP system in the CTD bay was left connected to the (unpowered) battery charger,
as well as to the two deck cables leading to the data acquisition computer and to the bench-top power supplies.
The male plug of the (disconnected) adapter cable between the battery and the LADCP star cable was dummied up.
While the deck cables in the wet lab were permanently connected to the acquisition computer with RS232-to-USB adapters,
the corresponding power connectors were left disconnected from the bench-top power supplies.
With this setup there is no voltage on any of the LADCP cables on the rosette.

A few minutes before the CTD was moved out of the bay for deployment the battery was disconnected from the charger and
connected to the ADCPs via an adapter cable and the star cable, both permanently installed on the rosette.
The male connector of the battery charger cable was dummied up.
In order to start data acquisition,the instruments were woken up by the acquisition computer,
the data from the previous cast deleted from their built-in memory cards, and the instruments were programmed to start pinging.
Finally the two deck cables were disconnected from the pig-tails that were also permanently installed on the
rosette in order to protect the expensive star cable from unnecessary wear.
The deck cables and pig tail connectors were dummied up and the latter were secured to the rosette with a velcro strap to avoid whipping during the casts.
Once everything was set up, the CTD operator and/or the marine tech were notified that the LADCP system was ready for deployment.
Deployment information was logged on LADCP log sheets once the CTD system had entered the water.

After the CTD had been secured in the bay after each cast the velcro securing the dummied up pig-tail ends  to the rosette was removed,
the dummied up pig-tail ends were rinsed with fresh water, the dummy plugs were removed, and the pig tails were connected to the deck cables.
Using the acquisition computer, LADCP data acquisition was stopped Afterand the data download was initiated.
Afterwards the two bench top power supplies were connected to the deck cables in the lab, the battery was disconnected from the adapter cable on the rosette,
the male end of the battery adapter cable on the rosette with two exposed pins now carrying 48V (from the bench-top power supplies) was dummied up,
and the battery cable was attached to the (still unpowered) charger cable.
Afterwards power was applied to the battery charger in the wet lab and the time noted on the LADCP log sheet.

After the data from the cast had finished downloading (after about 20 minutes on deep casts), the bench top power supplies were disconnected
from the deck cables in the lab. Then the data files were checked by integrating the measured vertical velocities in time,
which yields estimates for the maximum depth (zmax) and the end depth (zend) of the profile, both of which were recorded on the log sheet.
After the battery was fully charged (usually about an hour after charging was initiated, as indicated by LEDs on the charger)
the charger was disconnected from power in the wet lab and the time was noted on the log sheet.
At this stage, the LADCP system was ready for the next cast. 

Communication between the acquisition computer and the ADCPs was handled by a new acquisition software (acquire2),
implemented as a set of UNIX shell commands designed to minimize the possibility of operator errors.
Three different commands are used:

*Lstart* ??? This command wakes the instruments, lists their memory contents, clears the memory (after operator confirmation) 
and programs the instruments to start pinging by uploading command files.
CTD station and cast numbers must be provided by the operator since the LADCP files use an independent numbering scheme.
(CTD station and cast information, as well as the LADCP profile number were noted on the LADCP log sheet.)

*Ldownload* ??? This command interrupts the running data acquisition, downloads the data and backs up the data files to a network drive. 

*Lcheck* ??? This command integrates the measured vertical velocities from both ADCPs to estimate zmax and zend,
which are displayed together with other useful profile statistics before the data files are backed up (again) on the network drive.

While these three commands are all that is needed for LADCP data acquisition, a fourth command (Lreset) is available for
resetting the ADCPs after swapping instruments and in case of communications problems, of which there were none during this cruise. 

During the night watch the LADCP data were processed for horizontal velocity using the LDEO_IX processing software and for
vertical velocity using the LADCP_w processing software, both installed on the acquisition computer.
Important diagnostic plots were printed out, inspected, and filed in a ring binder.
In addition to these processing diagnostics, LADCP data quality was continuously monitored by creating section plots,
some of which can be found in the narrative section of this cruise report.
Over most of the section the LADCP data quality appears to be excellent, although there is a coverage gap in the deep waters of stations 
32-45 caused by insufficient acoustic backscatter due to lack of particles in the water column in the center of the subtropical gyre.
Inspection of the LADCP data from the 2012 occupation of A20 indicates similar problems in the same region, which are not flagged in the archived data, however.
A more comprehensive post-cruise LADCP QC will be carried out by Thurnherr in his lab before submission of the new data to the archives. 

.. figure:: images/A20_Sv.eps

  Data gap caused by insufficient acoustic backscatter for stations 32-45.


Instrumentation
---------------

A single 300kHz TRDI Workhose Monitor ADCP (WH300, s/n 12734), fitted with a custom self-recording accelerometer/magnetometer package,
was installed as the uplooker during all casts.
The data from the accelerometer/magnetometer package will be downloaded after the instruments return to the lab and used for QC and final processing if needed. 

Several different instruments were installed as downlookers during different casts.
For the shakedown cast (900) a prototype Nortek Signature 100 ADCP (Sig100) was used.
This instrument was provided as a loaner for testing.
It was integrated into the LDEO LADCP system during pre-cruise quarantine, requiring a re-write of the data acquisition software
and fabrication of an underwater adapter cable.
While the instrument had performed well on the bench in Falmouth, ping synchronization stopped working reliably on the vessel.
Since high-quality LADCP data can be collected without ping synchronization (requiring the detection and removal of the measurements affected
by interference) the shakedown cast was carried out with the two ADCPs pinging independently.
While the WH300 performed well, the Sig100 did not yield good data as indicated by bad values for zmax and zend.
The instrument was therefore replaced with a 150kHz TRDI Workhorse (WH150, s/n 19394) with a recently manufacturer-refurbished transducer. 

While the WH150 performed reasonably well, some of the processing diagnostic from the uplooker WH300 were noticably cleaner.
Therefore, before station 18 the WH150 was replaced with a second WH300 (s/n 24497).
This instrument performed very similar to the WH150, in particular showing the same (weak) anomalies in the processing diagnostics,
which are therefore likely related to the installation location (about 5 feet below the pivot point of the rosette) of the downlooker instrument.
As there was no apparent difference in the quality of the processed profiles before and after station 18 the WH300 (s/n 24497) was left installed until profile 31.

In the mean time the Sig100 data from the shakedown profile together with additional diagnostics were sent to the manufacturer for analysis.
Nortek engineers indicated that the poor data quality was caused by electrical noise and, in particular, 
by a missing ground path between the electronics and the pressure case.
The instrument was modified to provide such a ground path and installed again on the rosette for station 32.
Since the data from this station were noticeably improved, compared to the shakedown profile, it was decided to leave the
instrument on for another two profiles using different configurations (with and without ping synchronization) as well as with a different,
simpler, newly fabricated underwater adapter cable lacking the synchronization connections.
At the same time, a more careful analysis of the Sig100 data files was carried out, revealing that the quality of the recorded velocities was
still considerably worse than those from the TRDI instruments.
Therefore, the Sig100 was removed from the rosette and replaced by the WH150 used before on stations 1-17.

While this instrument performed well for a few casts its range deteriorated gradually but quite quickly to the
point of not returning any bins with valid velocities at depth on station 41.
The instrument was therefore replaced (again) for station 42 with the WH300 s/n 24497 which had been used before on station 18-31.
While this instrument yielded very good data, several profiles showed strange echo-amplitude anomalies affecting a small number of the recorded ensembles.
When, on station 52, the data from this instrument additionally contained an unexplained gap of 1.5s,
it was decided to swap the downlooker with another spare (WH300 s/n 24477).
This final instrument performed well and was left in place for the remainder of the cruise (profiles 53-90).
While WH300 s/n 24497 is suitable as a spare it was nevertheless decided decided to ship another instrument to port in the USVI for the following cruise (A22). 

While the Sig100 ADCP was not used any more, toward the end of the cruise a detailed engineering assessment of the data
From the prototype Sig100 was provided by Nortek engineers, with the following summary:

Unfortunately, the instrument proved to be missing key noise-reduction hardware, including shielding plates,
filter boards and ground connection, that caused noticeable range loss below 2000 m water depth.
And additional issue also artificially increased the noise in the first 100-150 m.
An on-site modification after the initial shakedown cruise (sic) significantly reduced the noise (correction of ground connection),
but proved to be insufficient to correct all issues and reach the design specifications.
However, data analysis does suggest near-instrument cells are still valid and that a properly built instrument should
have a range of approximately 100 m in deep, low scattering conditions, with no velocity bias.

While this overall optimistic assessment is encouraging, additional work during post-cruise QC will be required
to test the assertion that the velocity data from the near instrument cells (bins) are indeed valid. 