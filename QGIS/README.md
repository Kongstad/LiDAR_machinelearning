# QGIS 
![Screenshot](lidarxyz2_in.png)

## Establishing RGB data for LiDAR point cloud by extracting RGB information from optical satellite imagery

The data provided by the Danish authorities at https://dataforsyningen.dk/data/3931, contains LiDAR point cloud data for Denmark. The data is already clasiffied for the following classes:
* Unclassified
* Ground
* Low Vegetation
* Medium Vegetation
* High Vegetation
* Building
* Low Point (Noise)
* Reserved
* Water
* Bridge Deck
* High Noise

However, these labels have been applied automatically and some of them are not great for the purpose of training a model. The three vegetation classes are particularly troublesome. Boat piers and street lamps and bridges are often classified as either of the three vegetation categories, which is illustrated in the above image. 
The purpose of this QGIS section and for using QGIS is to add relevant RGB color channels to the point cloud for use in the machine learning features and to verify data. 


### Plugin installation for QGIS
--------------------------------------------------------------
First LAStools must be installed to QGIS, but it will not work properly unless you also install the LAStools standalone program on your system and point to the folder in the QGIS plugin configuration tab


### Steps
--------------------------------------------------------------
1) Load the LAZ (or las) file into QGIS.
2) Load in high quality optical satellite imagery that is shot from the same angle. 
3) Export this satellite image as a geotiff, with a DPI of 600 and a area layer extent to that of the LiDAR data
4) Whilst having selected the LiDAR laz data layer, use the LAStools plugin from the processing toolbox and select file - processing points, followed by lascolor. Add the input laz file, add the geotiff file in the second bracking and select an output file location, add a name and click run.
Note: Using an unlicensed version of LAStools means that the las file will lose some data. In this case the intensity values will be set to 0. The intensity value can be reimported from the original las file and reinstated via pandas dataframe, but this may cause inconsistencies in the data.

### Finished product
The image does a decent enough job, however it is ideal that the RGB values are derived from the remote sensing LiDAR source in form of a simultaneously snapped optical image. As this screenshot shows, the wrapping of the image to the point cloud is not ideal
![Screenshot](lidarxyz3_in.png)

