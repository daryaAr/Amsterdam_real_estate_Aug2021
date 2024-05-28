# Amsterdam_real_estate_Aug2021

In this project the aims are:

1. Having Statistical insight about the housing price in Amsterdam, Netherland, mostly focused on the discrits.
2. Having predictions about the housing price by using machine learning models.

For this project I am going to use the data of housing price in Amsterdam, in August 2021. You can find the used datasetby using this link: [Amsterdam House Price Prediction](https://www.kaggle.com/datasets/thomasnibb/amsterdam-house-price-prediction). This dataset contains about 924 housing entries with columns:
- Address
- zip code (Zip)
- Price
- Area
- Room
- Longitude (Lon)
- Latitude (Lat)

 The data types include integers for Room, and Area, floats for Price, Lon, and Lat; and objects (strings) for Address and Zip. Four entries have missing Price values.

Moreover, for this project I am also interested about the housing information in Amsterdam based on the districts (Stadsdeel). Since the Housing price dataset doesn't particularly provide the districts name, I am going to get the reqiured information about districts from open and confirmed database of Municipality of Amsterdam - Research, Information and Statistics [Amsterdam Districts](https://maps.amsterdam.nl/open_geodata/?k=192). This dataset includes District code,District name, Area_m2, and POLYGON data. The Coordinates are in WGS84.


Importing the dataset that includes the coordinates and geolocations of the districts of city Amsterdam.
Converting the Lon/Lat datas of the housing dataset to geometric objects.
Meging the districts dataset to housing dataset based on the geometric relationship.

