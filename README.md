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

Moreover, for this project I am also interested about the housing information in Amsterdam based on the districts (Stadsdeel). Since the Housing price dataset doesn't particularly provide the districts name, I got the reqiured information about districts from open and confirmed database of Municipality of Amsterdam - Research, Information and Statistics [Amsterdam Districts](https://maps.amsterdam.nl/open_geodata/?k=192). This dataset includes District code, District name, Area_m2, and POLYGON data. The Coordinates are in WGS84.

After having the housing price dataset and districts dataset, I merged them based on their geographical location (Lon and Lat) and created the desired dataset. To do so I followed these 3 steps:

1. Importing the dataset that includes the coordinates and geolocations of the districts of city Amsterdam.
2. Converting the Lon/Lat datas of the housing dataset to geometric objects.
3. Merging the districts dataset to housing dataset based on the geometric relationship.

You can find the codes in the [colab notebook of Amsterdam real estate districs Statistical insight](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/b809d34c14f36aaa9eae7386839149fa7806af14/Amsterdam_real_estate_districs_Statistical_insight.ipynb). Before starting the cleaning and analysing process, I added a new column to the data. I believe that having the information about the ratio of the price to the area (price per sqm) in the context of real estate is very helpful. Using this ratio is a very effective method, especially in finding outliers, since it allows us to identify properties that are significantly overpriced or underpriced relative to their size. This ratio helps normalize prices across different property sizes, providing a more standardized way to detect anomalies. So my dataset named "data" includes information about

- Address
- Zip	Price
- Area
- Room
- 	Lon
-  Lat
-  Stadsdeel (District name)
- 	Price_per_sqm

for each house entry. After this, I implied the cleaning methods e.g. removing missing values, and then started the statistical analysis of the data which you can find the report in [Report_Amsterdam_real_estate_statistical_analysis.md](Report_Amsterdam_real_estate_statistical_analysis.md).


