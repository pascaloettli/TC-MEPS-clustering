# TC-MEPS-clustering
This repository contains the data used in "An Objective Detection of Separation Scenario in Tropical Cyclone Trajectories Based on Ensemble Weather Forecast Data" by Oettli and Kotsuki (submitted to GRL).

Under "TC_centers", the data for the three tropical cyclones discussed in the paper can be found:
- 2020-12.DOLPHIN/  
- 2021-08.NEPARTAK/ 
- 2022-08.MEARI/

Each above directory contains 21 subdirectories, from 01 to 21 (one for each JMA-MEPS ensemble member), under which the files can be found. Each file has 14 positions of TC centers, in different referentiel:
- lon, lat: Longitude and latitude of the center in [°], World Geodetic System 1984 (EPSG:4326)
- X, Y: Easting and northing of the center in [m], JGD2011 / UTM zone 53N (EPSG:6690)
- X1, Y1: X and Y relative to the first position (Blender et al., 1997, 10.1002/qj.49712353910) at the first initialization and forecast times; Scaled by standard deviation in each direction

```
dimensions:
	time = 14 ;
variables:
	double time(time) ;
		time:standard_name = "time" ;
		time:long_name = "Forecast time" ;
		time:units = "minutes since 1970-1-1 00:00:00" ;
		time:calendar = "standard" ;
	float lon(time) ;
		lon:standard_name = "longitude" ;
		lon:long_name = "TC center longitude" ;
		lon:units = "degrees_east" ;
	float lat(time) ;
		lat:standard_name = "latitude" ;
		lat:long_name = "TC center latitude" ;
		lat:units = "degrees_north" ;
	float X(time) ;
		X:standard_name = "easting" ;
		X:long_name = "TC center easting" ;
		X:units = "meter" ;
	float Y(time) ;
		Y:standard_name = "northing" ;
		Y:long_name = "TC center northing" ;
		Y:units = "meter" ;
	float X1(time) ;
		X1:standard_name = "easting" ;
		X1:long_name = "scaled TC center easting" ;
		X1:units = "Relative location" ;
	float Y1(time) ;
		Y1:standard_name = "northing" ;
		Y1:long_name = "scaled TC center northing" ;
		Y1:units = "Relative location" ;
```
