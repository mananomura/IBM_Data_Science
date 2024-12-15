# IBM Data Science Capstone: SpaceX

## Introduction

![SpaceX Rocket Launch](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/api/Images/landing_1.gif)

---

### Background  
SpaceX has revolutionized the aerospace industry by significantly lowering the costs of space travel, making it more accessible. The company’s achievements include manned spaceflights, launching satellites for global internet access, and missions to the International Space Station. A key reason for its cost efficiency is the reusable first stage of its Falcon 9 rockets, bringing launch costs down to $62 million compared to $165 million for competitors. Predicting whether this first stage can be reused plays a crucial role in estimating the price of launches. Using public data and machine learning, we aim to predict first-stage reusability.

---

### Key Questions:
1. How do payload mass, launch sites, number of flights, and orbits influence first-stage landing success?  
2. How have success rates changed over time?  
3. Which predictive model best classifies successful landings?

---

## Executive Summary  

This project identifies factors contributing to successful rocket landings. The approach involves:  
- **Data Collection:** Using SpaceX REST API and web scraping to gather data  
- **Data Wrangling:** Creating a binary success variable  
- **Exploration:** Visualizing factors like payload mass, launch site, flight frequency, and annual trends  
- **Analysis:** Using SQL to compute statistics such as payload ranges for successful launches  
- **Visualization:** Highlighting geographical factors influencing launch site success  
- **Modeling:** Building predictive models, including logistic regression, SVM, decision trees, and KNN  

---

## Results

### Data Insights:
- Success rates have improved over time.  
- The KSC LC-39A site boasts the highest success rate.  
- Certain orbits (ES-L1, GEO, HEO, SSO) consistently achieve 100% success.

### Geographical Observations:
- Launch sites are near the equator, offering cost-saving benefits due to Earth's rotational speed.  
- All sites are coastal, facilitating easier rocket retrieval.

### Predictive Models:
- All models performed similarly, with the decision tree model slightly outperforming others.

---

## Methodology

### Data Collection via API:
- Data requested from SpaceX API and processed into dataframes.  
- Missing values for Payload Mass were replaced with the mean.  

### Data Collection via Web Scraping:
- Falcon 9 launch data extracted from Wikipedia using BeautifulSoup.  
- Data organized into a structured dataframe and exported to CSV.

### Data Wrangling:
- Landing outcomes converted into binary format: 1 (successful) or 0 (unsuccessful).

### Exploratory Data Analysis (EDA):
- Charts and visualizations created to analyze relationships between factors.  
- SQL queries performed to derive insights into payload ranges and outcomes.  

### Mapping and Dashboards:
- Maps created using Folium to visualize launch sites and their proximities.  
- Dashboards designed with Plotly Dash to display success metrics.

### Predictive Analytics:
- Data standardized and split into training and test sets.  
- Models built using GridSearchCV for parameter optimization.  
- Algorithms tested: Logistic Regression, SVM, Decision Trees, and KNN.  
- Performance evaluated using metrics like Jaccard Score, F1 Score, and Accuracy.

---

## Conclusion

### Key Findings:
- **Launch Success Trends:** Success rates have improved over time.  
- **Geographical Advantage:** Launch sites near the equator and coast aid in cost reduction and reusability.  
- **Optimal Launch Site:** KSC LC-39A achieves the highest success rates, especially for payloads under 5,500 kg.  
- **Orbit Success Rates:** Orbits ES-L1, GEO, HEO, and SSO consistently succeed.  
- **Payload Mass Impact:** Higher payload masses correlate with increased success rates.

### Recommendations:
1. **Expand Dataset:** A larger dataset will improve model reliability and result generalization.  
2. **Advanced Feature Analysis:** Use techniques like PCA to refine predictive capabilities.  
3. **Consider XGBoost:** Testing advanced models like XGBoost may enhance accuracy.  
