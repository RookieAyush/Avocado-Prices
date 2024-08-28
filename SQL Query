# Avocado-Prices
Analyze the prices of Avocado across regions, states, districts and other parameters 
# Find the regions with the highest average avocado prices over the entire dataset.
SELECT
  region,
  AVG(AveragePrice) AS average_price
FROM `Avocado_Price.avocado_price` 
GROUP BY region 
ORDER BY average_price DESC 
LIMIT 10;

#Find the years with the highest total avocado sales volume.
SELECT
  year,
  SUM(TotalVolume) AS total_volume
FROM `Avocado_Price.avocado_price`
GROUP BY year
ORDER BY total_volume DESC
LIMIT 10;

#Find the avocado types with the highest average price over the entire dataset.
SELECT
  type,
  AVG(AveragePrice) AS average_price
FROM `Avocado_Price.avocado_price`
GROUP BY type
ORDER BY average_price DESC
LIMIT 10;

#What is the total volume of avocados sold in each region, grouped by type?
SELECT region, type, SUM(TotalVolume) AS Total_Volume_Per_Region_Per_Type
FROM `Avocado_Price.avocado_price`
GROUP BY region, type;

#What is the correlation between the average price and total volume of avocados sold in each region, grouped by year?
SELECT region, year, CORR(AveragePrice, TotalVolume) AS Correlation_Price_Volume_Per_Region_Per_Year
FROM `Avocado_Price.avocado_price`
GROUP BY region, year;

#Find the variance of the average price of avocados.
SELECT
  VAR_SAMP(AveragePrice) AS variance
FROM
  `Avocado_Price.avocado_price`;
