DNA sequencing is becoming cheaper and easier to conduct with every passing year, but it is still prohibitively expensive to sequence community DNA, collect samples and time consuming to analyze. We already have large datasets of sequences analyzing the phytoplankton community all around the world, so what if we can predict the phytoplankton community using environmental variables?
In this code I will attempt to develop a model that uses environmental variables in the Beaufort Sea measured during a cruise that followed transects over the shelf break, to predict the ratio of diatoms to dinoflagellates.

The files and scripts needed are: 

THE FOLLOWING 3 SCRIPTS SHOULD BE RUN IN ORDER TO REPLICATE RESULTS
- Einarsson_DAnalysis_Prelim_895Project.ipynb
  - This script cleans up and pools the data from the various sources used. Sources are explained below and in the script.
- Einarsson_Plotting_Mapping.ipynb
  - This script plots and visualizes the data to determine range and spatial distribution of the data collected.
- Model_Einarsson.ipynb
  - This script develops and tests a model to predict the ratio of diatoms to dinoflagellates using environmental variables.

Data files needed:
- fluro_turner_wHeader.txt
- Sik_Sal.csv
- Sikuliaq_model_Grouped.csv
- R2R_ELOG_skq201713s_FINAL_EVENTLOG_20180913_174843.csv
- Buoy_NOAA_data.txt
- Alldata_withSSTSSSsatallite.csv
- etopo1_bedrock_BeaufortSea_1.nc
- RVSikuilaq2017Log_Edited.csv

The data used from other sources include fluorometric and log data from R2R: 
https://www.rvdata.us/search/cruise/SKQ201713S
The fluorometer and NASA remote sensing data files used in this code are hosted on Dropbox:
https://www.dropbox.com/sh/b3773gnsm2fx61b/AAD0XKkozEUIBjskAO6Jccpla?dl=0
NOAA weather buoy data:
https://www.ndbc.noaa.gov/view_text_file.php?filename=prda2h2017.txt.gz&dir=data/historical/stdmet/
ETOPO bathymetry data:
https://maps.ngdc.noaa.gov/viewers/wcs-client/
Satellite remote sensing data from NASA:
https://podaac-tools.jpl.nasa.gov/drive/files/allData/modis/L3/terra/4um/v2019.0/9km/daily/2017
https://podaac-tools.jpl.nasa.gov/drive/files/allData/smap/L3/RSS/V4/8day_running/SCI/2017
