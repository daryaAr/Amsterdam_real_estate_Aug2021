### This report is based on my calculations in this colab notebook:
[Amsterdam_real_estate_districs_Statistical_insight](Amsterdam_real_estate_districs_Statistical_insight.ipynb)

After doing the preprocessing steps on my dataset which is mentioned in [README.md](README.md), the data was ready to start for analyzing.

In the first step, I created the first look on the Price, Area, Number of Rooms, and Price per Square meter.
</p>

![Histogrmas](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/main/plots/hist.png?raw=true)

</p>

## A Summary of Histograms:

### 1. Histogram of Price:
- The distribution of housing prices is highly skewed to the right, indicating that most properties are priced below 1 million Euros. A significant tail extends to higher prices, reaching up to 6 million Euros. The kernel density estimate (KDE) line further highlights the skewness and the presence of a few high-priced outliers.

### 2. Histogram of Area:
- The area of the properties also shows a right-skewed distribution, with most properties having an area between 50 and 100 square meters. The KDE line shows a peak around 75 square meters and a gradual decline, with a few properties extending up to 600 square meters.

### 3. Histogram of Room:
- The number of rooms per property is roughly normally distributed, centered around 3-4 rooms. There is a noticeable peak at 3 rooms, and the distribution tapers off for properties with more than 5 rooms, extending up to 14 rooms. The KDE line indicates a single peak corresponding to the most common number of rooms.

### 4. Histogram of Price per Square Meter:
- The price per square meter distribution shows multiple peaks, indicating variability in property pricing. The main concentration is around 4000 to 7000 Euros per square meter. The KDE line highlights these peaks and the presence of some properties with significantly higher price per square meter, extending up to 25,000 Euros.

These histograms provide a comprehensive overview of the data, illustrating the distribution of property prices, areas, number of rooms, and price per square meter. The skewness in prices and area indicates the presence of a few high-end properties, while the distribution of rooms shows that most properties have a moderate number of rooms. The variability in price per square meter suggests different pricing strategies that can be because of other factors like the neighborhood or property types within the dataset. Therefore, more visualizations especially based on districts can be helpful.
</p>

After visualizing the histograms, it was time to handle the outliers. To do so, I used the data from column **"Price_per_sqm"**, instead of just **"Price"**, since it provides a more standardized way to detect anomalies. I used the 1.5*IQR method for finding the outliers. Below you can see the comparison of the box plot of price/sqm before and after removing the outliers.
</p>

![Comparison of box plots of price/sqm](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/main/plots/comp_outlier_ratio%20(1).png?raw=true)

</p>

Then I got more visualizations based on districts. For example the scatter plot on Amsterdam's map, gives a good insight about the distribution of houses and their price.
</p>

![Scatter map](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/main/plots/scatter_map%20(1).png?raw=true)

</p>

## A summary of the Scatter Plot of House Prices per sqm in Amsterdam:

1. **Geographical Distribution:**

- Central Amsterdam, especially around the inner city and canal belt, shows a higher concentration of properties with mid to high prices per square meter, indicated by the prevalence of orange and red points.
- Outlying districts such as Nieuw-West, Noord, and Zuidoost exhibit more blue and purple points, indicating relatively lower prices per square meter.

2. **Density and Clustering:**

- The central and southeastern parts of Amsterdam have a dense clustering of property listings, suggesting higher demand and property availability in these regions.
- Areas like West, Oost, and parts of Centrum have a high density of points, reflecting a larger number of listings and potentially higher property values.

This visualization provides a detailed and interactive overview of the housing market in Amsterdam, showcasing the distribution and pricing of properties across different neighborhoods. It highlights the varying affordability and density of housing, offering valuable insights for potential buyers, investors, and policymakers.

To get insights from different point of view, in the next step I Calculated the average area for each district and also created the box plot of  price/sqm for each district.
</p>

![comp_area_ratio](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/main/plots/comp_area_ratio.png?raw=true)

</p>

# Insights:
These two plots together provide insights into the housing market in different districts, focusing on the average area and price per square meter (Price_per_sqm). By comparing these two plots we find out:

 1. **Higher Prices in Smaller Areas:**
- **Centrum:** Despite having one of the largest average areas, it also shows high prices per square meter. This indicates high property values in the central district, likely due to its central location and amenities.
- **Zuid:** High price per square meter suggests that this district is one of the most expensive areas in Amsterdam, reflecting its desirability.

2. **Affordable Districts with Smaller Areas:**

- **Zuidoost and Nieuw-West:** These districts have lower prices per square meter and also smaller average areas, indicating more affordable housing options.

3. **Balanced Districts:**

- **Noord and West:** These districts show a balance with moderate average areas and median prices per square meter. They offer a mix of affordability and space.

4. **Outliers:**

- Outliers in the price per square meter plot indicate that even in generally affordable districts, there are properties with exceptionally high prices.


By analyzing both plots together, we can conclude that while some districts like Zuid and Centrum offer large areas at high prices, others like Zuidoost and Nieuw-West provide more affordable housing with smaller areas. This combined insight helps in understanding the trade-offs between space and cost across different parts of Amsterdam, aiding potential buyers or investors in making informed decisions.

Finally, for the last step, I tried to find the relation between the affordability of districts and their popularity. To do so, I Calculated the affordability of districts based on average price/sqm, and also Calculated the popularity of districts of districts based on their frequency.

</p>

![pop afford](https://github.com/daryaAr/Amsterdam_real_estate_Aug2021/blob/main/plots/comp_pop_afford.png?raw=true)

</p>

# Insights:

1. **High Popularity and High Cost:**

- **West and Centrum:** These districts show a correlation between high popularity and high costs. Despite the higher prices per sqm, these areas remain in high demand.

2. **Balanced Districts:**

- **Oost and Noord:** These districts offer a balance between affordability and popularity. They have moderate prices per sqm and a reasonable number of listings.

3. **Affordable but Less Popular:**

- **Nieuw-West and Zuidoost:** These districts are more affordable but are less popular compared to other districts. They could be attractive for budget-conscious buyers.

4. **Least Popular and Affordable:**

- **Weesp:** This district, while being one of the most affordable, has the least number of listings, indicating lower demand or fewer available properties.




