# GEOM99 Web GIS
## Technical Activity Log 3 - Week 12

### Task1. Group Project Data Preprocessing
1. Time sheet 
  * Date and time: Mar 22, 2-4pm
  * Total hours: 2 hrs

2. Technical details (summary)
  * Report to Shawn
  * Group discussion and comments
    - Check in and work update and combine
    - Reflection on progress and Shawn's suggestions

3. Outcomes (what you completed) 

4. Next steps
  * Live data for earthquakes 
  * Middle tier editing: join two feature layers (so Canada and the US don't have to show in separate pie chart/gauge in dashboads)
  * Figure to auto update the live date for csv (python)
  * NASA's FIRMS data (WFS, WMS, KML)

5. Resources (links, reminders, etc.)
  * AGOL hosted feature layer allows data join (item detail > create view layer > joined view layer)


### Task2. Lecture and Lecture Content Review
1. Time sheet 
  * Date and time: Mar 25, 4-5pm
  * Total hours: 1 hrs

2. Technical details (summary)
  * FOSS vs. COTS
    - Intermix
  * Open source web GIS 
    - esri fGDB: GeoPackage
    - OpenSphere
    - Geonode
    - etc.


### Task3. Group Project Data Preprocessing 2
1. Time sheet 
  * Date and time: Mar 28, 6-10:30pm
  * Total hours: 4.5 hrs

2. Technical details (summary)
  * Keep trying to update live data to the web
    - NASA FIRMS import with WFS
      i. [Requested for a map key](https://firms.modaps.eosdis.nasa.gov/mapserver/wms-info/#firms-mapkey)
      ii. Canada MODIS 7 days fires/hotspots as a trial, [Ingest into AGOL](https://firms.modaps.eosdis.nasa.gov/tutorials/wfs_arcgis_online/)
        + Question. ![showing Canada fires in the US](https://Venusqh.github.io/geom99TechLogs/log3fig1.JPG)
      iii. [Update layer with a certain time interval](https://doc.arcgis.com/en/arcgis-online/create-maps/set-refresh-interval-mv.htm)
      + Able to successfully update live data! 
    - NASA FIRMS import with KML
      + KML/KMZ are static files, cannot be directly used to update live data to AGOL the same way as dynamic feature services. 
      + ![Google Earth Pro](https://Venusqh.github.io/geom99TechLogs/log3fig2.JPG) supports auto-refresh, but ArcGIS Dashboards doesn't support
      + Insert URL: https://firms.modaps.eosdis.nasa.gov/data/active_fire/modis-c6.1/kml/MODIS_C6_1_USA_contiguous_and_Hawaii_24h.kml
      + This one doesn't work for live
      + A Web Feature Service (WFS) is primarily a feature access service, also includes elements of a feature type service, a coordinate conversion/transformation service and a geographic format conversion service. 
      However, clients have no administrative rights over the data, can only retrieve or modify the data of the specific feature(s) but not the complete file. 
      + WFS operations (11: grouped as discovery operations, query operations, locking operations, transaction operations and operations to manage stored parameterized query expressions)
  * Dashboard
    - Improve visualization and interactive interface
      + Add a collapsible sidebar for hazard ![date and number selection](https://Venusqh.github.io/geom99TechLogs/log3fig3.JPG) (user is able to hide or pin on the side of the main interface, doesn't hurt the aesthetic)
      + A gauge to display the magnitude of multiple events in decending order (the giant number can effectively alert users to current hazards while offering the flexibility to toggle between multiple features without occupying excessive space)
  * Probability of engaging other hazards (data sources)
    - Earthquake
      + Living Atlas [Recent Earthquakes](https://mcmaster.maps.arcgis.com/home/item.html?id=9e2f2b544c954fda9cd13b7f3e6eebce) (live)
      + USGS [Earthquake Hazards Program](https://www.usgs.gov/programs/earthquake-hazards) (live when access)
      + Natural Resources Canada [All earthquakes of the last 30 days](https://www.earthquakescanada.nrcan.gc.ca/recent/maps-cartes/index-en.php?tpl_region=canada#events) (live when access)
  * Took a look at NRCAN live wildfire data again but unable to retrieve valuable outputs

3. Outcomes (what you completed) 
  * Able to engage real live wildfire data of North America in two ways: add layer from living atlas, and import with WFS URL

4. Next steps
  * Check in with group members
  * Need to move on to the next step: write a website explaining/documenting the process (problem statement, methodology, solution and team info)

5. Resources (links, reminders, etc.)
  * Most links are attatched in previous writing for easy reading
  * [WFS reading](https://natural-resources.canada.ca/earth-sciences/geomatics/canadas-spatial-data-infrastructure/standards-policies/8934)
  * More. If time allowed, NASA FIRMS has a tutorial on [data ingest and manipulation in python](https://firms.modaps.eosdis.nasa.gov/content/academy/data_ingest/firms_data_ingest.html) (this is about update live data through csv files, and edit data in the data tier)


#### Total Time: 7.5 hrs