# Yiren-590Assignment6
The dataset of this project is mainly used to analyze the median_house_value, which contains some key characteristics that affect house prices, such as median_income, geographic location (longitude, latitude) and housing characteristics (total_rooms, housing_ median_age, etc.). The goal of the dataset is to construct a model to predict median house prices from these characteristics.

### Attribute Information
1) median_income: median_income, a numeric variable indicating the average income level of residents in the area and the characteristic that has the greatest impact on housing prices.
2) longitude: longitude, a numeric variable indicating the geographic location of the area where the house is located (east-west).
3) latitude: latitude, a numeric variable indicating the geographic location of the area where the house is located (north-south direction).
4) total_rooms: total number of rooms in the house, a numeric variable indicating the size of the house.
5) housing_median_age: median age of the houses, numeric variable indicating the average age of the houses in the area.
6) population: total population, numeric variable indicating the number of inhabitants in the area.
7) ocean_proximity: categorical variable indicating the distance of the house from the ocean, e.g. “near the ocean” or “inland”.
8) median_house_value: target variable, numeric variable indicating the median house price, which is the value we need to predict.

### Model
I used a **random forest regression model** to predict the median house price. Through feature processing and model training on the training set, the model can effectively capture the relationship between features and target variables. During the model construction process, I used cross-validation to ensure the generalization performance of the model and improved the prediction accuracy by adjusting the model parameters.

### Plot
**PDP（Partial Dependence Plot）and ICE（Individual Conditional Expectation）:** PDP and ICE is used to analyze the impact of characteristics such as median_income on median house prices.PDP shows the average impact, while ICE shows the individual differences for each sample. The results show that as median_income increases, the median house price shows a significant upward trend, especially in the middle-income range.

**ALE（Accumulated Local Effects）:** The ALE plot overcomes the limitations of the PDP in dealing with feature correlations and more accurately demonstrates the localized impact of features on house prices.The ALE plot shows that median_income has the greatest impact on house prices in the middle-income range, with a diminishing effect in the upper-income range.

**Permutation Importance:** The importance of each feature for house price prediction was analyzed and it was found that median_income was the most important feature, followed by geographic location (LONGITUDE and LATITUDE), which verified the importance of income and location for house price.

### Conclusion
By constructing and analyzing the house price prediction model, median_income and geographic location (longitude and latitude) are the most significant features affecting the median house price. both the PDP and ALE plots show that income has a positive effect on house price, especially in the middle-income range, where it has the most significant effect on house price enhancement. The ALE plot, on the other hand, better handles feature correlation and is able to explain the impact of features more precisely. The feature importance analysis further demonstrates the central role of income and location in house price prediction. These analyses provide a strong basis for future optimization of house price prediction models, and also provide an effective reference for decision-making in the real estate industry.
