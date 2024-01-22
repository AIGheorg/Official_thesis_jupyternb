# Official_thesis_jupyternb
Based on the location of your receiver and for the moment of time:
To run this code, pick a tile from https://www.geotiles.nl/ and download the alamanac from https://www.navcen.uscg.gov/gps-nanus-almanacs-opsadvisories-sof - check for the correct week of the survey mission

Before running this code, please filter the data based on the height of your receiver using LAStools:
las2las -i pc.LAZ -drop-z-below [antenna-height] -o pc-height-filter.LAZ

Then create a lasindex file:
lasindex -i pc-height-filter.LAZ

Modify in the second block of the notebook the user input with the data of your receiver and then run all the blocks. Also modify the filter_pointcloud function and insert in com_string1 the point cloud you are using. Modify also in the 17th block (main block) the moment of time for your measurement.

The rest after the main block is some testing to understand the data and the plotting of the DoP values - it is not necessary to run them.
