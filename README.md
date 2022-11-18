# QGIS, Python and LiDAR data
Using QGIS, Python and LiDAR data from Copenhagen as input, machine learning models are generated and tested on new data.

![Screenshot](/QGIS/3d_render_training_set.png)

## Overview
* LiDAR laz files has been downloaded from Dataforsyningen (https://dataforsyningen.dk/data/3931) covering a 1 square kilometer area of Copenhagen.
* RGB layers were added through QGIS by using optical satellite maps and the tool LAStools.
* Using jakteristics module to determine additional point cloud features: Omnivariance, Planarity, Verticality.
* Python were then used to load the data and test several machine learning methods to increase the accuracy in predicting objects such as buildings, medium- and high vegetation and ground. A spatially similar validation data set, but from a different area of Copenhagen and thus with different structures, was used to see how the model reacts to new data. In order to improve its accuracy and robustness to new data, a small part of the validation set is used to strengthen the model. The models are evaluated by the metrics: Precision, recall, f1 score and overall accuracy.


## Steps
1) [Acquire LiDAR data (External link)](https://dataforsyningen.dk/data/3931) 
2) [QGIS guide](https://github.com/Kongstad/LiDAR_machinelearning/blob/main/QGIS/README.md)
3) [Jakteristics Notebook](https://github.com/Kongstad/LiDAR_machinelearning/blob/main/Jakteristic/jakteristic.ipynb)
4) [Machine learning - Jupyter Notebook](https://github.com/Kongstad/LiDAR_machinelearning/blob/main/Python/liDAR_MachineLearning.ipynb)
