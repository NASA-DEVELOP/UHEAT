==================================
GEE Scripts for URBAN HEAT EXPOSURE ASSESSMENT TEMPE (UHEAT) Analysis
==================================

Date Created: November 3, 2020


This code allows the user to retrieve environmental variables for a given study area from Landsat 8
and MODIS sensors. They can be retrieved for a group of years, each year, or monthly. All *Retrieve scripts 
are functions to be called in the *AggSatData and SatMonthly scripts. You MUST have a Google Earth Engine 
(GEE) profile ready to go before running these scripts. 

======================================
 Required Packages
======================================
* GEE Profile and GEE files/scripts to copy and past these scripts to. 

======================================
 Parameters
======================================

1. Create a GEE profile.
2. Copy and paste text files into GEE scripts.
3. Be sure to upload the Tempe Shapefile under Fall2020_Assets in GEE.
4. Start with 1_Fall2020_AZ_TempeII_AggSatData and edit it to call the 2_***_Retrieve scripts. 
5. Click run!

======================================
 Contact
======================================
Name(s): Blake Steiner
E-mail(s): blake.a.steiner@gmail.com

======================================
 Files
======================================
1. 1_Fall2020_AZ_TempeII_AggSatData: Script to collect and process aggregated or yearly satellite data.

2. 2_Fall2020_AZ_Retrieve_***: The Retrieve scripts are all functions that are called by _AggSatData and 
	_SatMonthly scripts. These functions have a built-in cloud and water mask and retrieve data from 
	Landsat 8 and AQUA MODIS satellites.  

3. 3_Fall2020_AZ_TempeII_SatMonthly: Script to collect and process monthly satellite data.

4. 3_Fall2020_AZ_Tempe_TimeSeries_LST: Script to create a short time series of LST in a study area. 
	This script can be adapted for NDVI as well. It is also independent of all other scripts.




	