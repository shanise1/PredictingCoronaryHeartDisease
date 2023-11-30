# Predicting Coronary Heart Disease
[The Erdős Institute](https://www.erdosinstitute.org/) Fall 2023 Bootcamp

by Henri Antikainen, Rachel Appel, Melanie King, Sriram Raghunath, Shanise Walker

# Project Description and Goal
Heart disease is the leading cause of death in the United States (US) and the most common type of heart disease is coronary heart disease. Each year many families and individuals are impacted by diagnoses of coronary heart disease or death caused by coronary heart disease. There are a number of risk factors and lifestyle choices that can put people at risk for developing coronary heart disease. While many people may understand the biological or medical risk factors that place them at higher risks for developing coronary heart disease, there is still a gap in understanding how lifestyle choices and cultures also impact the development of coronary heart disease. Some people are not even aware that heart disease is preventable [[1]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1994011/#:~:text=Some%20are%20not%20even%20aware,(Rogers%20et%20al%202000)).

# Project Goal
The goal of this project is to use predictive modeling techniques to determine which risk factors and lifestyle choices features impact and place people at higher risk for developing coronary heart disease. 

# Dataset
The dataset is gathered from the  Center for Disease Control and Prevention’s Interactive Atlas of Heart Disease and Stroke (IAHDS) [online mapping tool](https://www.cdc.gov/dhdsp/maps/atlas/index.htm). County-level data for 3226 counties in the United States is gathered on coronary heart disease. The dataset consists of 59 features-including 5 risk factors, 14 social, economic, and environmental features, 12 demographic features, 21 healthcare delivery and insurance features, and 4 healthcare costs features. The data for each feature was gathered from a variety of sources between 2016-2020 and placed into the IAHDS interactive mapping tool. The [features key](https://github.com/shanise1/PCD/blob/main/Dataset%20Features%20Key.pdf) provides a detail description of each feature.  

# Model Approach 
Three predictive models created using three different analysis techniques--XGBoost, Gaussian Naïve Bayes, and Linear Regression--were developed to assess coronary heart disease risk factors and lifestyle choices. Each model was trained at the state-level for counties before being aggregated and tested at the continental level. We then compared the accuracy of each of the continental models primarily using mean squared error to determine the best fit model for further analysis.

Below is a diagram of our complete modeling approach.  
![model](images/modelapproach.png)

# Results 
Using the mean squared error, we measured the accuracy of each predictive model. The XGBoost provided the most accurate model, and thus, its findings are reported here.  According to the XGBoost model, the top three risk factors that predict coronary heart disease are: having high cholesterol, being in a household without a computer, and being 25+ years old without a 4-year college degree. Our model provides insights into coronary heart disease risk factors and demonstrates that access to education and technology impacts health. By increasing access to education and technology, communities can help reduce the likelihood of getting coronary heart disease.  See image below for the complete list of feature importances of risk factors for coronary heart disease using the XGBoost model.

![xgboostresults](images/xgboostresults.png)

# Future Work
Our results focused on risk factors influencing coronary heart disease at the continental level. However, it is likely that these risk factors vary in importance based on individual differences within the US states. To better understand these differences, we propose that case studies be conducted on individual states. Some states lack access to healthcare resources more than other states.  Some states lack access to healthcare resources more than other states. Future project expansion hopes to capture these healthcare resource discrepancies. Further exploration can also be done on states with the highest (e.g., Ohio) and lowest (e.g., Nevada) predictive accuracy (as measured by MSE) in our XGBoost model. Understanding why the states varied in predictive accuracy can help strengthen the model. 

# References
[1] Safeer RS, Cooke CE, Keenan J. The impact of health literacy on cardiovascular disease. Vasc Health Risk Manag. 2006;2(4):457-64. doi: 10.2147/vhrm.2006.2.4.457. PMID: 17323600; PMCID: PMC1994011.
