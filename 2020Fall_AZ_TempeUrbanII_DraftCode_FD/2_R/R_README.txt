==================================
R Scripts for URBAN HEAT EXPOSURE ASSESSMENT TEMPE (UHEAT) Analysis
==================================

Date Created: November 3, 2020


This code allows the user to derive socio-economic variables from the 
AZ_Tempe_UDII_Fall2020_TidyCensus script and create the UHEAT scores from
the AZ_Tempe_UDII_Fall2020_PrincipalComponentAnalysis_UHEAT script. You must run 
the GEE and _TidyCensus scripts first before the _PrincipalComponentAnalysis_ script.
Note that there is an R image, UHEAT_data_Rimage, file that has an example of what
the R variables should look like.  

########################################################################
#                                   ROUTINE 
#                   1_AZ_Tempe_UDII_Fall2020_Tidycensus.R
#
#				   RUN FIRST (hence the 1 in the name)
#-----------------------------------------------------------------------
#
# Description: This first part of this routine extracts and processes socio-economic 
#             variables from American Census Survey (ACS) by census tract or block group for
#             the city of Tempe and saves them to a csv file. The variables produced
#             match those included from previous literature.  
#             Finally the data set are merged and saved in a common csv file.
#             
#             Users can define year, census type, working directory, and geography. 
#             
#             NOTE: the code take ~10 minutes to run 
# Code Requirements: This script requires installation of "tidyverse","tidycensus","foreign","sf" 
#                    See the Setup libraries section for more info.
#
# Created by: Lance Watkins, Ph.D. School of Geographical Sciences and Urban Planning
#             Arizona State University
#
# Modified by: Blake A Steiner
# Date created: Oct. 15, 2020
# History:  
#           Oct. 15, 2020 - bas - created to extract census data from tidy census
#           Oct. 22, 2020 - bas - modified code to fit context of Tempe
#           Oct. 29, 2020 - bas - Reran code for testing and edited it
########################################################################

########################################################################
#                            ROUTINE 
#     2_AZ_Tempe_UDII_Fall2020_PrincipalComponentAnalysis_UHEAT.R
#
#			    RUN SECOND
#-----------------------------------------------------------------------
#
# Description: This script calculates (1) a heat exposure score, 
# (2) a heat vulnerability score and (3) a heat priority score by census tract 
# for the City of Tempe using Principal Component Analysis. 
# The script was adapted from vulnerability-index.RMD by Mary Wright, 
# ASU and from the Spring 2020 AZ-Philadelphia project. The output is saved as a csv file.
#
# Running this script requires the following input files:
#         - Socioeconomic data as written out by 
#           AZ_Tempe_UDII_Fall2020_TidyCensus.R
#           (filename TMP_UHEAT_CENSUS_VARIABLES_*_*_CT_ALLVariables_ALLMetrics_2020-10-22.csv
#         - Satellite retrieved nLST, dLST, NDVI, NDBI, NDWI and albedo 
#           data as written out by Google Earth Engine script 
#           Fall2020_AZ_TempeII_AggSatData (filename (Median_EnvVar_2015_2020_*.csv)
#
# Created by: Charlotte C. Wagner (ccwagner88@gmail.com)
# Date created: March 10, 2020
#
# Modified by: Blake A. Steiner (blake.a.steiner@gmail.com)
# Date modified: Oct. 13, 2020
#
# History: 2020, Mar 10 - ccw - adapted script from vulnerability-index.RMD
#          2020, Mar 21 - ccw - added heat exposure and heat vulnerability index
#          2020, Oct 13 - bas - modified code for just heat exposure index for Tempe 2020
#          2020, Oct 25 - bas - modified code to take in new vulnerability variables for Tempe 2020
#          2020, Oct 29 - bas - edited code to be neater
#          2020, Nov 16 - bas - fixed row ordering issue in output
########################################################################

======================================
Tutorial Description
======================================
In order to reproduce this work, a word document file will describe the steps on how to
run the code is provided in the main directory.
