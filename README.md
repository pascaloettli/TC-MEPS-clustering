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
