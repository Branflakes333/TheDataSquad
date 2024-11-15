# Project Paper Outline:

# Comparative Analysis of Housing Prices: US vs. London

**Course:** STAT 580 – Multivariate Analysis  
**Instructor:** Ryan Lafler  
**Group Members:**

* Brandon Miner  
* Diego Angulo Nevarez  
* Jihyun Do  
* Xinnan Li

**Date:** 11/13/24

---

# Abstract

This study aims to analyze and then compare housing markets between various cities in the United States to London. Using data from Zillow for U.S. housing market data and Arnav Kulkarni’s dataset on “Kaggle.com” for London housing prices, as well as supplementary dataset from the US Census Bureau, the analysis seeks to identify similarities in housing trends and factors affecting home prices across these regions. Methodologies include Principal Component Analysis (PCA), cluster analysis, and t-tests to determine patterns and significant differences in pricing factors. The study will utilize statistical programming in R and SAS, employing libraries, but not limited to, `tidyverse` for data manipulation, visualization, and statistical testing. Preliminary findings suggest potential price clustering and factor differentiation between the two regions, providing insight into how global and regional economic factors impact housing affordability.

---

# I. Introduction

* **Background & Motivation**  
  * Overview of current housing market trends in the U.S.  
  * Importance of comparing U.S. markets with a major international city, London, for a broader understanding of housing dynamics.  
  * The housing market is a critical component of economic stability, personal wealth, and societal well-being. With property values and rental rates affecting individual and national finances in the current state of the market, housing costs have become a focal point of socio-economic studies.  
  * This study aims to reveal geographic differences to identify similarities and unique factors in housing trends between these two regions, with the goal of exploring patterns, price dynamics, and possible socio-economic impacts.   
* **Research Questions**  
  * Which U.S. cities have similar housing market characteristics to London?  
  * How do factors such as size, location, and neighborhood characteristics influence housing prices differently in the US compared to London?  
  * Are there notable differences between U.S. and London housing markets in terms of average price and influencing factors such as size and location?  
* **Scope & Limitations**  
  * The study focuses on housing prices, affordability, and influencing factors between selected US cities and London. It includes a comparative analysis of average prices, size, geographic location, and other accessible variables influencing housing affordability.  
  * Limitations in currency conversions and data timeliness across regions.  
  * Challenges in matching comparable market indicators between datasets.  
  * The availability and timeliness of data across regions may vary, making it challenging to capture identical time frames and economic events for both regions.  
* **Hypotheses**  
  * **Hypothesis 1:** Home prices in London are generally higher than those in the U.S.  
  * **Hypothesis 2:** Significant differences exist between U.S. and London housing markets due to distinct economic and geographic factors.

  ---

  # II. Methodologies

* **Data Sources**  
  * U.S. housing data sourced from Zillow.  
  * Supplementary housing data sourced from US Census Bureau.  
  * London housing data sourced from Kaggle.  
* **Variables and Transformations**  
  * Key variables include, but are not limited to; `RegionID`, `RegionName`, `Price`, and date-specific price variables, as well as income levels and other factors that may provide further insight on impacts on housing prices and/or affordability.  
  * Reshaping data for comparison and reducing dimensionality for effective PCA.  
* **Statistical Techniques**  
  * **Exploratory Data Analysis (EDA):** Summary statistics and visual comparisons.  
  * **Multivariate Analysis Techniques:** PCA, cluster analysis, and ANOVA/t-tests.  
  * **Regression Modeling:** Predictive modeling for price factors.  
  * **Decision Tree (CV / RF):** Classification of London(test) trained on US(train)

  ---

  # III. Exploratory Data Analysis (EDA)

* **Summary Statistics**  
  * Mean, median, standard deviation, and interquartile range for key variables (i.e., housing price by region and/or city from Zillow and London Kaggle dataset, as well as supplementary US Census Bureau dataset).  
* **Visualization**  
  * Box plots, histograms, and scatter plots to reveal data distributions and detect potential outliers, and comparte housing prices across cities and/or regions. Heatmaps for correlations between variables may be helpful as well. Zillow and Kaggle datasets would be used to illustrate this, with the supplement of the US Census Bureau dataset to showcase the income levels variables.  
* **Geospatial Analysis**  
  * Maps showing price distributions by region and/or city, property type, property size, etc. that could be impactful. This could be done using, for instance, R’s ggplot2 libraries for geographic data.

  ---

  # IV. Analysis

* **Multivariate Analysis**  
  * **PCA:** Identifying principal components that influence housing price variance. This will be useful for various variables such as income level by regions.  
  * **Cluster Analysis:** Segmenting cities with similar housing market characteristics.  
    * Identify which US city(ies) are statistically similar to London  
    * K-Means: For cities with well-defined housing market tiers (i.e., low, middle, and high).  
    * DBSCAN: For areas where market segments might not be clearly separated or might include outliers.  
* **Comparative Statistical Tests**  
  * ANOVA/t-tests for comparing price means between U.S. cities and London.  
  * Regression models to evaluate predictor strength for housing prices.  
  * Chi-Square Test of Independence for categorical data (e.g., region, property type, number of bedrooms, etc.)  
* **Regression Modeling**  
  * Multiple Linear Regression: To assess which factors (e.g., number of bedrooms, income level, region or city, property type, property size) predict housing prices. Including interaction terms could provide insights into combined effects, such as how both city and size influence price.  
* **Machine Learning Approaches**  
  * Random Forest Regressor: Necessary if the dataset is viewed too complex for previous approaches  and will use this method that will offer robust predictive power for pricing.  
  * Decision Trees: This can provide an interpretable model of factors impacting pricing differences, which may help communicate findings effectively to non-technical audiences.

  ---

  # V. Results

* **Descriptive Results**  
  * Statistical summaries for both U.S. and London markets.  
  * Boxplots comparing price distributions by city.  
* **Inferential Results**  
  * Insights from PCA on dominant price factors in each market.  
  * Cluster Analysis and ANOVA/t-test findings on market segmentation.

  ---

  # VI. Concluding Remarks

* **Summary of Findings**  
  * Overview of key trends and differences in housing prices between U.S. cities and London.  
  * Factors that impact housing price and/or affordability according to insights discerned in the datasets.  
* **Re-state Abbrev. Limitations**  
  * Data coverage limitations, currency challenges, and assumptions in the analyses.  
* **Future Research Suggestions**  
  * Expanding to other international markets and incorporating macroeconomic factors.

  ---


  # VII. References

* Zillow. (n.d.). *Zillow Home Value Index (ZHVI)*. Zillow. Retrieved November 12, 2024, from [https://www.zillow.com/research/data/](https://www.zillow.com/research/data/)  
* Kulkarni, A. (2020). *Housing prices in London* \[Dataset\]. Kaggle. Retrieved November 12, 2024, from [https://www.kaggle.com/datasets/arnavkulkarni/housing-prices-in-london](https://www.kaggle.com/datasets/arnavkulkarni/housing-prices-in-london)  
* United States Census Bureau. (n.d.). *Financial Characteristics for Housing Units With a Mortgage*. United States Census Bureau. Retrieved November, 2023, from [https://data.census.gov/table/ACSST1Y2023.S2506?q=housing+affordability+in+United+States](https://data.census.gov/table/ACSST1Y2023.S2506?q=housing+affordability+in+United+States)    
* United States Census Bureau. (n.d.). *Financial Characteristics for Housing Units Without a Mortgage*. United States Census Bureau. Retrieved November, 2024, from [https://data.census.gov/table/ACSST1Y2023.S2507?q=housing+affordability+in+United+States](https://data.census.gov/table/ACSST1Y2023.S2507?q=housing+affordability+in+United+States)   
  ---

  # VIII. Authors' Bios

* **Brandon Miner** is a fifth-year undergraduate student at San Diego State University, majoring in Statistics with an emphasis in Data Science and minoring in Mathematics. He has developed strong skills across the data analysis pipeline, from data wrangling to predictive modeling, as well as proficiency in Python and R. Currently in his final semester, Brandon has professional experience working with public policy data as an intern at the San Diego County Taxpayers Association. As he prepares for graduation, Brandon is eager to apply his skills in a data science career across a variety of industries.  
* **Diego Angulo Nevarez** is a fourth-year student at San Diego State University, majoring in Statistics with a focus in Data Science. His interests lie in applying statistical analysis and predictive modeling to better understand mental health and human behavior. Diego has experience in college law enforcement, where he analyzed local crime data to support initiatives aimed at improving campus safety. He’s now shifting his focus to educational data, exploring areas like transfer student demographics, retention rates, and academic success. Proficient in R, SAS, and Python, Diego hopes to be well-equipped for a career in data-driven analysis and insight into a field that will help improve quality of life.  
* **Jihyun Do** is a third-year undergraduate student majoring in General Biology with a minor in Statistics at San Diego State University. Her academic interests focus on ecological data analysis and statistical modeling, particularly using programming languages such as R and SAS. With a strong foundation in both biology and quantitative methods, Jihyun has gained hands-on experience in analyzing ecological datasets, conducting statistical tests, and applying advanced modeling techniques to explore patterns in biodiversity and ecosystem dynamics.  
* **Xinnan Li** is a graduate student in biostatistics at San Diego State University. His interests lie in biostatistical analysis and statistical models to better understand the laws of bioinformatics. He focuses on visualizing data and is proficient in R and SAS statistical software. Currently in his second year, Xinnan has interned at ABB.inc in San Jose and has experience working with multiple sets of data. His hope is that he learns to better promote data development

---

### IX. Contact Information

* **Brandon Miner:** Email: \[bminer5476@sdsu.edu\], LinkedIn: \[[linkedin.com/in/brandonminer](http://linkedin.com/in/brandonminer)\], GitHub: \[[https://github.com/Branflakes333](https://github.com/Branflakes333)\]   
* **Diego Angulo Nevarez:** Email: \[dangulonevarez5690@sdsu.edu\], LinkedIn: \[[linkedin.com/in/diego-angulo-654625328](http://linkedin.com/in/https://www.linkedin.com/in/diego-angulo-654625328) \]  
* **Jihyun Do:** Email: \[jdo4550@sdsu.edu\], LinkedIn: \[[linkedin.com/in/jihyundo](http://linkedin.com/in/jihyun-do-3022501a4)\]  
* **Xinnan Li:** Email: \[xli1479@sdsu.edu\], LinkedIn: \[linkedin.com/in/xinnan-li-010533180\]

