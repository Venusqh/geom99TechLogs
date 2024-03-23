# GEOM99 Web GIS
## Technical Activity Log 2 - Week 11

### Task1. Group Project Data Preprocessing
1. Past activities
Meeting with Shawn in the lab and got some suggestions on the project. The problem statement was approved later over the week. 

2. Time sheet 
  * Date and time: Mar 15, 2-4pm
  * Total hours: 2 hrs

3. Technical details and Outcomes (summary)
  * The project is focusing on reporting natural hazards happening in the US. We aim to utilize the ArcGIS web platforms: AGOL for data management and web mapping, Dashboards for data direct showcasing and StoryMap for background and information. 
  * Here are some gathered data sources: 
    - Living Atlas [web map]
      + USA Current Wildfires 
      + USA Storm Reports 
    - NASA's FIRMS [KML, WFS and WMS for live, shp and csv for 'live when download'] 
      + Concerns: (1) Includes false active fire data, e.g. powers stations - more like hotspots map; (2) worldwide 
    - FireSmoke [web map]
      + Predict fire for 30h prior
    - Note. It is hard to find and apply live data into web solutions, tried my best to engage live, there were also data where either live when downloaded, or from very recent times. 

4. Next steps
  * Engage Canadian data source
  * Figure out a best method to add data to the web

5. Resources (links, reminders, etc.)
  * [View the Living Atlas feature layer item](https://fleming.maps.arcgis.com/home/item.html?id=d957997ccee7408287a963600a77f61f)
  * [Download the NASA data here](https://firms.modaps.eosdis.nasa.gov/usfs/active_fire/)
  * [Download the FireSmoke data here](https://firesmoke.ca/forecasts/current/)


### Task2. Lecture and Lecture Content Review
1. Time sheet 
  * Date and time: Mar 18, 4-5pm
  * Total hours: 1 hr

2. Technical details (summary)
  * Configure vs. custom web solutions
    - Esri company scale
    - ArcGIS Solutions
    - Case. Simcoe County WebGIS 
    - Other open-source solutions for the three tiers

3. Outcomes (what you completed) 
  * Never used ArcGIS Solutions before, good resource
  * Better understanding on the three tiers and platform functions
  * Simcoe County impressive open source solution


### Task3. Group Project Data Preprocessing 2
1. Time sheet 
  * Date and time: Mar 21, 4-6pm
  * Total hours: 2 hrs

2. Technical details (summary)
  * Focus on active wildfires and tornados in <ins>Canada</ins> and the US: 
  * Searching for Canada data: 
    - Living Atlas [web map]
      + Active Wildfires in Canada 
      + Active Wildfire Perimeters in Canada 
      + Satellite (MODIS) Thermal Hotspots and Fire Activity 
        + (Worldwide)
    - WesternU Northern Tornados Project [csv, shp, GeoJSON]
      + Data from 2017-2023
    - Natural Resources Canada [csv, WMS, web map]
  * Adding from Esri source to web map
    - Directly add > browse layers > Living Atlas
  * Adding csv and filter to web map
    - I first used ArcGIS Pro > 'xy to point' > 'extract by mask' > share 
      + But executing on local software failed requirements with the web
    - AGOL > new item > upload from device > create a hosted feature layer
  * Adding WFS to web map
    - AGOL > new item > URL > paste WFS link > "Service does not exist or is inaccessible"
      + [Tutorial for ingesting in Pro](https://firms.modaps.eosdis.nasa.gov/usfs/tutorials/wfs_arcgis_pro/)
      + Unable to add NASA's FIRMS live wildfire data
  * Adding WMS to web map
    - AGOL > new item > URL > paste WMS link > select layers to add
      + Unable to show in MapViewer bc "MAP_KEY is invalid or you have exceeded the transaction limit" 
      + The data added was past 24/48/72 hours or 7 days, can't update 
      + Unable to add NASA's FIRMS live wildfire data
  * Reverse engineered to retrieve data source from web map (FireSmoke)
    - f12 inspect > network > type 'rest' > refresh
      +  Nothing valuable

3. Outcomes (what you completed) 
  * A web map item on AGOL engaging data layers and good visuals ready for use

4. Next steps
  * Meet with Shawn in the lab
  * Figure how to filter the data to North America only <ins>on web</ins>
  * Try to find active tornado data of Canada
  * Don't give up NASA's FIRMS data, two ways: learn to import KML, or [request a free map key](https://firms.modaps.eosdis.nasa.gov/mapserver/usfs/wms-info/) for WMS
  * Try reverse engineer the NRCAN data (a different method from adding csv directly)

5. Resources (links, reminders, etc.)
  * [View the Living Atlas feature layer item](https://fleming.maps.arcgis.com/home/item.html?id=21638fcd54d14a25b6f1affdef812146)
  * [Download the NTP data here](https://ntpopendata-westernu.opendata.arcgis.com/)
  * [Download the NRCAN data here](https://cwfis.cfs.nrcan.gc.ca/datamart/metadata/activefires)
  * Other links attatched in previous sections for easier reading


### Task4. Pratical Lab 
1. Time sheet 
  * Date and time: Mar 21&22
  * Total hours: 2.5 hrs

2. Technical details and Outcomes 
  * Timed question quiz
  * 2 Documentations


#### Total Time: 8 hrs
