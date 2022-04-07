==================================
Folders for URBAN HEAT EXPOSURE ASSESSMENT TEMPE (UHEAT) Analysis
==================================

Date Created: November 10, 2020

These four folders contain the source code and assets necessary to repeat the UHEAT 
analysis. First one that should be looked at is 1_GEE. Once that is completed, the second 
set of scripts in 2_R can be modified and used. In the Fall2020_Assets folder, there are 
three subfolders. It has an example folder for the user to double check there inputs with
images of successful runs. There is a Tempe_CensusTracts folder that contains a .dbf 
census tract file for use in the TidyCensus R Script under the 2_R folder. 
The last subfolder is the Tempe_Shapefile. This is used as an asset in the 1_GEE script
to clip the satellite data to the study area and census tracts. The fourth folder contains 
video tutorials for each of the main scripts. 

======================================
 Contact
======================================
Name(s): Blake Steiner
E-mail(s): blake.a.steiner@gmail.com

======================================
 Files
======================================
1. 1_GEE: A folder that contains all GEE scripts and a GEE specific README. Please look at this
	set of files first. 

2. 2_R: A folder that contains the two R scripts to collect census data and analyze all data 
	with the principal component analysis. It also contains an R specific README. Please run 
	this second. 

3. Fall2020_Assets: This folder contains example images of successful runs, a census tract .dbf
	file to be used in the R Tidycensus script, and Tempe census tract shapefile that must be uploaded
	to GEE in order to run GEE scripts.

4. Video_Tutorials: This folder contains three subfolders, one for each major script/platform.
	They are numbered in the order they should be viewed and in the order the code should 
	run in. Each video is about an hour long and goes over, line by line, the code.  

======================================
Tutorial Description
======================================

-------------
Steps
-------------

1. Open up the word document tutorial and follow it along with the videos.  
	
