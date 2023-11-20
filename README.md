# Probablistic-Modelling-of-Time-Series-StreamflowData
Undertook a project focused on Probabilistic Modeling of Streamflow Data to predict the extent  of natural calamities such as Extreme Floods

### Motivation

There is a need to understand and predict extreme events such as floods or droughts. These events can have significant impacts on human societies and ecosystems, and their frequency and intensity may be affected by climate change. By analyzing historical data and developing probabilistic models, we can better predict these events and inform strategies for risk management and adaptation. This is a crucial area of research with significant implications for both policy making and public safety. 

I have selected the Polavaram gauging site as dataset. Polavaram is significant due to the construction of the Polavaram Dam, which is a multi-purpose project aimed at providing irrigation, hydroelectric power, and flood control to the region. The dam is expected to have a significant impact on the economic, social, and environmental development of the region. An analysis like this will be extremely helpful for Engineers to plan the grade of materials to be used, cost of construction and other factors for building a hydraulic project.

### Methodology

1. Data Preparation: Imported your data from a CSV file which contains data from Polavaram gauging site streamflow values of the Godavari river, dropped any missing values, and converted the 'Date' column to a datetime format.
2. Extreme Value Analysis (EVA): Initialized the EVA model with your data using the pyextremes library in python
3. Extracting Extreme Values: Extracted extreme values using the Block Maxima (BM) method with one-year blocks.
4. Fitting the Model: Fitted a Generalized Extreme Value (GEV) distribution to the extreme values.
5. Model Evaluation: Got the model parameters such as AIC, likelihood
6. Estimating Return Levels: Estimated the 100-year return level and printed it along with its 95% confidence interval.
7. Return Value Summary: Obtained return values for various return periods (2, 5, 10, 20, 50, 100, 200, 500, 1000 years) and stored them in a summary for cross validation.
8. Plotting: Finally, I have plotted the model diagnostics and return value plot for visual assessment of the model.

### Results

I have trained a GEV model with 
-----------------------------------------------
free parameters: loc=25589.632, scale=10273.651
AIC: 1147.540
loglikelihood: -571.650
-----------------------------------------------

The 100-year return level is 72849.95789780281 m³s¯¹ with the 95% confidence interval: [64398.92240662832, 80472.42385681237]

### Discussion

The graphical results along with this analysis are attached as a separate folder in the main.

The R-squared values you obtained are quite high (0.985 and 0.986), which indicates that the fitted model explains a large proportion of the variance in your data. This suggests that the Generalized Extreme Value (GEV) distribution is a good fit for my block maxima values.

The p-values you obtained are 0.0, which is less than the commonly used significance level of 0.05. This indicates that the fit of the GEV distribution to your data is statistically significant.
However, it's important to remember that these are just statistical tests and they have their limitations. They do not prove that your data follows a GEV distribution, they just provide evidence to support this hypothesis. It's always a good idea to use additional methods such as the kolmogorov smith test.
