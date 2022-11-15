# QGIS 

### Establishing RGB data for LiDAR point cloud by extracting RGB information from optical satellite imagery

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

However, these labels have been done automatically and some of them are not great for the purpose of training a model. But I have chosen to filter them out in the python section later on. The purpose here is to 

