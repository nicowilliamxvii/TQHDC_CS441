

# World Happiness Report Data Analysis

 1. Introduction

Happiness is an important indicator of quality of life and well-being in different countries around the world. Governments, researchers, and policy makers often analyze happiness levels to better understand the social, economic, and political conditions that influence people's well-being.

This project analyzes the **World Happiness Report 2017** to explore global happiness patterns. The dataset contains information about happiness scores for countries as well as several socio-economic factors that may influence happiness, including economic conditions, health, freedom, social support, and trust in government.

The objective of this project is to apply data analysis and visualization techniques to better understand the distribution of happiness across countries and identify the key factors associated with higher happiness levels.



 2. Research Questions

This project aims to answer the following research questions:

1. Which countries have the highest and lowest happiness scores?
2. How is happiness distributed across countries worldwide?
3. What factors are most strongly associated with happiness levels?
4. Do different regions of the world show differences in happiness levels?
5. Is there a relationship between economic conditions and happiness?

---

 3. Dataset Description

The dataset used in this project is the **World Happiness Report 2017**, published by the United Nations Sustainable Development Solutions Network.

The data was collected through the Gallup World Poll and includes survey responses from individuals in over 160 countries and multiple languages.

Each country in the dataset is assigned a **Happiness Score**, which is derived from several contributing factors:

* GDP per capita (Economy)
* Social support (Family)
* Healthy life expectancy (Health)
* Freedom to make life choices (Freedom)
* Generosity
* Perception of corruption (Trust)
* Dystopia residual (baseline comparison)

In addition, the dataset includes information about job satisfaction levels in each country.

These variables allow researchers to investigate how different economic, social, and political factors contribute to happiness levels across the world.

---

 4. Methodology

 4.1 Data Processing

The dataset was imported and analyzed using the Python programming language. The data was first loaded into a DataFrame structure to inspect the dataset and understand the available variables.

Several preprocessing steps were performed before analysis:

* Checking the number of observations
* Inspecting column names and data types
* Identifying and handling missing values
* Ensuring that numerical variables were correctly formatted

Basic numerical summaries such as mean, minimum, and maximum values were also calculated to gain an overview of the dataset.

---

 4.2 Data Analysis Approach

To answer the research questions, several analytical methods were applied.

First, the happiest and least happy countries were identified by ranking countries based on their Happiness Score.

Second, the dataset was grouped by region to examine differences in happiness levels across geographic areas.

Third, several visualizations were created to better understand patterns in the data. These visualizations include bar charts, histograms, scatter plots, and correlation analysis.

These methods allow us to explore both the distribution of happiness and the relationships between happiness and its contributing factors.

---

5. Data Analysis and Visualization

 5.1 Top and Bottom Happiest Countries

Countries were sorted according to their Happiness Score to identify the top 10 happiest countries and the bottom 10 least happy countries.

A horizontal bar chart was used to visualize the happiness scores of the top countries. This visualization helps illustrate the differences in happiness levels among countries.

The results show that countries with stronger economies, better healthcare systems, and stronger social support networks tend to rank higher in happiness.

---

 5.2 Regional Comparison of Happiness

To understand regional patterns, the dataset was grouped according to the Region variable.

The average happiness score was computed for each region and regions were ranked from most happy to least happy.

This analysis helps reveal geographical patterns in happiness levels and shows that some regions consistently report higher happiness scores than others.

---

 5.3 Distribution of Job Satisfaction

A histogram was created to examine the distribution of job satisfaction levels among countries.

The data was divided into categories ranging from 40% to 100% job satisfaction. This visualization helps illustrate how job satisfaction varies globally and how it may relate to overall happiness.

---

 5.4 Relationship Between Happiness and Other Factors

Scatter plots were used to examine the relationship between Happiness Score and other variables such as GDP per capita, health, freedom, and social support.

These visualizations help reveal potential relationships between economic and social factors and happiness levels.

---

 5.5 Correlation Analysis

A correlation analysis was performed to determine which variables are most strongly associated with the Happiness Score.

The correlation coefficients between happiness and other variables were calculated to identify the factors that have the strongest relationship with happiness.

---

 6. Key Findings

Several important insights were identified through the analysis.

First, happiness levels vary significantly across countries. Some countries consistently rank among the happiest while others have much lower happiness scores.

Second, economic factors such as GDP per capita appear to have a strong relationship with happiness levels.

Third, social support and health also play important roles in determining happiness. Countries with strong social networks and better healthcare systems tend to report higher happiness scores.

Finally, regional differences were observed, suggesting that geographic, economic, and cultural factors influence happiness levels.

---

 7. Conclusion

This project analyzed global happiness patterns using the **World Happiness Report 2017**.

The results indicate that happiness is influenced by a combination of economic, social, and health-related factors. Countries with stronger economies, better health systems, and stronger social support networks tend to report higher happiness levels.

The analysis also highlights significant regional differences in happiness levels across the world.

Overall, data visualization and statistical analysis provide valuable insights into the factors that contribute to human well-being.

---

 8. Appendix

 Code Implementation

The Python code used for data processing, analysis, and visualization is included in this section or provided through the project repository.

The analysis was implemented using:

* Python
* pandas
* matplotlib
* seaborn

