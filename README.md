# QGIS, Python and LiDAR data
Using QGIS, Python and LiDAR data from Copenhagen as input and through semantic segmentation, testing several machine learning methods.

## Overview
* LiDAR laz files has been downloaded from Dataforsyningen (https://dataforsyningen.dk/data/3931) covering a 1 square kilometer area of Copenhagen.
* RGB layers were added through QGIS by using optical satellite maps and the tool LAStools.
* Using jakteristics module to determine additional point cloud features: Omnivariance, Planarity, Verticality
* Python were then used to load the data and test several machine learning methods through semantic segmentation to increase the accuracy in determining the classes such as buildings, bridge deck, vegetation and ground. 
* A spatially similar validation data set, but from a different area of Copenhagen and thus with different structures, was used to see how the model reacts to new data. In order to improve its accuracy and robustness to new data, a small part of the validation set is used to strengthen the model


## Steps
1) [Acquire LiDAR data](https://dataforsyningen.dk/data/3931) 
2) [QGIS guide](https://github.com/Kongstad/LiDAR_machinelearning/blob/main/QGIS/README.md)
3) [Jakteristics Notebook](https://github.com/Kongstad/LiDAR_machinelearning/QGIS/readme.md)
4) [Jupyter Notebook](https://github.com/Kongstad/LiDAR_machinelearning/QGIS/readme.md)
