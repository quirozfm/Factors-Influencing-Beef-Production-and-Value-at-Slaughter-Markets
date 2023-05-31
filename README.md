# From Soybean Fields to Slaughter Markets: Uncovering the Hidden Connections in Beef Production
------------------------------------------------------------------------------------------------------------------------------
This regression project will focus on total value of beef at slaughter market (measured in billions of dollars), based on data
from the    and the impact the following variables could have on annual production:
------------------------------------------------------------------------------------------------------------------------------

    • Average Temperature
    • Average Precipitation
    • Barley Production
    • Maize Production
    • Sorghum Production
    • Soya Beans Production
    • Cattle Population
    • Meat Consumption

I will begin with my hypotheses and a regression will run with all 8 variables and we will remove
insignificant variables manually one by one. Next, I will run the regression models again with associated interpretations of
the data. I will run the SPSS stepwise regression model, which will initially include all 8 variables so the software can
determine the most optimal regression model for what affects the total value of beef at the slaughter market. Lastly, I will
discuss the method of data collection, and any biases that may affect the individual variables, as well as the overall data
set. 

## Section I: Hypotheses and Rationale
_______________________________
In the following sections, I will test these hypotheses by running regression models, analyzing the results, and adjusting
the models accordingly.

    Of note, for interpretation purposes, my working statistical test hypotheses are as follows:
    
    • H0: the tested variables do not affect the total value of beef at the slaughter market.
    • H1: the tested variables do affect the total value of beef at the slaughter market. 
___________________________________________
# Section II: Regression Model with all 8 Variables

[View All Variables PDF](images/All%20Variables.pdf)


#### Correlation Analysis:
The correlation matrix provides the Pearson correlation coefficients for all pairs of variables. Some notable correlations
are:

    -   Beef_Value_SlaughterMarket has a strong positive correlation with SoyaBeans (0.686, p<0.001)
        and moderate positive correlations with Maize (0.536, p=0.007) and Barley (0.492, p=0.014).
        
This suggests that as the production of these crops increases, the value of the beef slaughter market tends to increase as well.

    -   Beef_Value_SlaughterMarket has a moderate negative correlation with BeefConsumption_US (-0.637, p=0.001).
    
Indicating, that as beef consumption in the US increases, the value of the beef slaughter market tends to decrease.

#### Regression Analysis:
A multiple linear regression model has been fitted with Beef_Value_SlaughterMarket as the dependent variable and all other variables as predictors.

    - The model has an R-Square of 0.814, meaning that 81.4% of the variance in Beef_Value_SlaughterMarket. 
    - This model has a statistically significant F-value of 6.015 (p=0.004), overall, the model is a good fit.
    - Among the predictors, BeefConsumption_US (B = -7.256, p=0.009) and SoyaBeans (B = 0.004, p=0.023) have 
      statistically significant coefficients. 
      
This means that for every unit increase in BeefConsumption_US, the Beef_Value_SlaughterMarket tends to decrease by 7.256 units, while for every
unit increase in SoyaBeans, the Beef_Value_SlaughterMarket tends to increase by 0.004 units.

    -  The other predictors in the model are not statistically significant, indicating that they may not have a strong relationship
       with the Beef_Value_SlaughterMarket.

In summary, the analysis suggests that there is a strong relationship between the value of the beef slaughter market and the production of SoyaBeans, as well as an inverse relationship with BeefConsumption_US. The other variables do not appear to have a significant impact on the beef slaughter market value. However, the presence of multicollinearity in the model
indicates that these results should be interpreted with caution. To address this issue, we will proceed with manually removing non-significant variables individually. 

___________________________________________
# Section III: Manual Removal of Variables

## Model Summary:

The model summary indicates that the adjusted R-squared is 0.689, which means that approximately 68.9% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor variables (AvgTemp, BeefConsumption_US, Sorghum, Beef_Production_BillionPounds, Barley, Maize, and SoyaBeans). The model's standard error of the estimate is 6.83518, which reflects the average distance that the observed values fall from the regression line.

## ANOVA:

The ANOVA table shows that the model is statistically significant at a 0.002 level. This means that there is a significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The F-value of 7.013 indicates that the model is a good fit to the data, as it is significantly different from a model with no predictors.

## Coefficients:

The coefficients table provides information about the relationship between each predictor variable and the dependent variable (Beef_Value_SlaughterMarket).

    - BeefConsumption_US: The coefficient is -7.135, with a p-value of 0.008, indicating a 
      significant negative relationship between BeefConsumption_US and  Beef_Value_SlaughterMarket.
      As BeefConsumption_US increases by 1 unit, the Beef_Value_SlaughterMarket decreases by 7.135 units, 
      holding other variables constant.

    - Beef_Production_BillionPounds: The coefficient is 0.637, with a p-value of 0.764, indicating no
      significant relationship between Beef_Production_BillionPounds and Beef_Value_SlaughterMarket.

    - Barley: The coefficient is -0.001, with a p-value of 0.206, indicating no significant relationship
      between Barley and Beef_Value_SlaughterMarket.

    - Maize: The coefficient is 0.000, with a p-value of 0.705, indicating no significant relationship 
      between Maize and Beef_Value_SlaughterMarket.

    - Sorghum: The coefficient is 0.000, with a p-value of 0.698, indicating no significant relationship
      between Sorghum and Beef_Value_SlaughterMarket.

    - SoyaBeans: The coefficient is 0.004, with a p-value of 0.023, indicating a significant positive 
      relationship between SoyaBeans and Beef_Value_SlaughterMarket. As SoyaBeans increase by 1 unit, 
      the Beef_Value_SlaughterMarket increases by 0.004 units, holding other variables constant.

    - AvgTemp: The coefficient is -0.326, with a p-value of 0.889, indicating no significant 
      relationship between AvgTemp and Beef_Value_SlaughterMarket.

From here, we will continue to remove those variables with the highest p-values.

---

## Regression – No Precipitation, No Avg Temperature

### Model Summary:

The model summary indicates that the adjusted R-squared is 0.712, which means that approximately 71.2% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor variables (BeefConsumption_US, Beef_Production_BillionPounds, Barley, Maize, Sorghum, and SoyaBeans). The model's standard error of the estimate is 6.57258, which reflects the average distance that the observed values fall from the regression line.

### ANOVA:

The ANOVA table shows that the model is statistically significant at a <0.001 level. This means that there is a significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The F-value of 8.846 indicates that the model is a good fit for the data, as it is significantly different from a model with no predictors.

### Coefficients:

The coefficients table provides information about the relationship between each predictor variable and the dependent variable (Beef_Value_SlaughterMarket).

    - BeefConsumption_US: The coefficient is -7.154, with a p-value of 0.006, indicating a 
      significant negative relationship between BeefConsumption_US and Beef_Value_SlaughterMarket.
      As BeefConsumption_US increases by 1 unit, the Beef_Value_SlaughterMarket decreases by 7.154 units, 
      holding other variables constant.

    - Beef_Production_BillionPounds: The coefficient is 0.691, with a p-value of 0.730, indicating 
      no significant relationship between  Beef_Production_BillionPounds and Beef_Value_SlaughterMarket.

    - Barley: The coefficient is -0.001, with a p-value of 0.182, indicating no significant relationship
      between Barley and Beef_Value_SlaughterMarket.

    - Maize: The coefficient is 0.000, with a p-value of 0.713, indicating no significant relationship 
      between Maize and Beef_Value_SlaughterMarket.

    - Sorghum: The coefficient is 0.000, with a p-value of 0.694, indicating no significant relationship 
      between Sorghum and Beef_Value_SlaughterMarket.

    - SoyaBeans: The coefficient is 0.003, with a p-value of 0.005, indicating a significant positive 
      relationship between SoyaBeans and Beef_Value_SlaughterMarket. As SoyaBeans increases by 1 unit, 
      the Beef_Value_SlaughterMarket increases by 0.003 units, holding other variables constant.

For further analysis, we will continue to remove the highest p-values (Barley, Maize, and Sorghum) and rerun the regression analysis until we achieve only the significant variables (BeefConsumption_US and SoyaBeans).

### Regression – No Precipitation, No Avg Temperature, No Beef Production

### Model Summary: 
The model summary indicates that the adjusted R-squared is 0.730, which means that approximately 73% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor variables (BeefConsumption_US, SoyaBeans, Sorghum, Barley, and Maize). The model's standard error of the estimate is 6.36361, which reflects the average distance that the observed values fall from the regression line.

### ANOVA:
The ANOVA table shows that the model is statistically significant at a <0.001 level. This means that there is a significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The F-value of 11.297 indicates that the model is a good fit to the data, as it is significantly different from a model with no predictors.

### Coefficients:

The coefficients table provides information about the relationship between each predictor variable and the dependent variable (Beef_Value_SlaughterMarket).

    -   BeefConsumption_US: The coefficient is -6.650, with a p-value of <0.001, indicating a significant
        negative relationship between BeefConsumption_US and Beef_Value_SlaughterMarket.
        As BeefConsumption_US increases by 1 unit, the Beef_Value_SlaughterMarket decreases by 6.650 units, 
        holding other variables constant.
    
    -   Barley: The coefficient is -0.001, with a p-value of 0.180, indicating no significant relationship
        between Barley and Beef_Value_SlaughterMarket.
    
    -   Maize: The coefficient is 0.000, with a p-value of 0.719, indicating no significant relationship  
        between Maize and Beef_Value_SlaughterMarket.
     
    -   Sorghum: The coefficient is 0.000, with a p-value of 0.522, indicating no significant relationship 
        between Sorghum and Beef_Value_SlaughterMarket.
        
    -   SoyaBeans: The coefficient is 0.004, with a p-value of 0.002, indicating a significant positive 
        relationship between SoyaBeans and  Beef_Value_SlaughterMarket. As SoyaBeans increases by 1 unit,
        the Beef_Value_SlaughterMarket increases by 0.004 units, holding other variables constant.

### Regression – No Precipitation, No Avg Temperature, No Beef Production, No Maize

## Model Summary: 

The model summary indicates that the adjusted R-squared is 0.730, which means that approximately
73% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor
variables (BeefConsumption_US, Barley, Sorghum, and SoyaBeans). The model's standard error of the estimate is
6.36361, which reflects the average distance that the observed values fall from the regression line.
ANOVA: The ANOVA table shows that the model is statistically significant at a <0.001 level. This means that there is a
significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The
F-value of 11.297 indicates that the model is a good fit to the data, as it is significantly different from a model with no
predictors.

## Coefficients: 

The coefficients table provides information about the relationship between each predictor variable and the
dependent variable (Beef_Value_SlaughterMarket).

    -   BeefConsumption_US: The coefficient is -6.592, with a p-value of <0.001, indicating a significant negative 
        relationship between BeefConsumption_US and Beef_Value_SlaughterMarket. As BeefConsumption_US increases 
        by 1 unit, the Beef_Value_SlaughterMarket decreases by 6.592 units, holding other variables constant.
    
    -   Barley: The coefficient is -0.001, with a p-value of 0.165, indicating no significant relationship
        between Barley and Beef_Value_SlaughterMarket.
    
    -   Sorghum: The coefficient is 0.000, with a p-value of 0.325, indicating no significant relationship
        between Sorghum and Beef_Value_SlaughterMarket.
    
    -   SoyaBeans: The coefficient is 0.003, with a p-value of <0.001, indicating a significant positive
        relationship between SoyaBeans and Beef_Value_SlaughterMarket. As SoyaBeans increases by 1 unit,
        the Beef_Value_SlaughterMarket increases by 0.003 units, holding other variables constant. 

#plots00000000000000000000

### Regression – No Precipitation, No Avg Temperature, No Beef Production, No Maize, No Sorghum

## Model Summary:

The model summary indicates that the adjusted R-squared is 0.745, which means that approximately
74.5% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor
variables (BeefConsumption_US, Barley, and SoyaBeans). The model's standard error of the estimate is 6.18394, which
reflects the average distance that the observed values fall from the regression line.

## ANOVA: 

The ANOVA table shows that the model is statistically significant at a <0.001 level. This means that there is a
significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The
F-value of 19.547 indicates that the model is a good fit to the data, as it is significantly different from a model with no
predictors.

## Coefficients:

The coefficients table provides information about the relationship between each predictor variable and the
dependent variable (Beef_Value_SlaughterMarket).

    -   BeefConsumption_US: The coefficient is -7.055, with a p-value of <0.001, indicating a significant negative relationship
        between BeefConsumption_US and Beef_Value_SlaughterMarket. As BeefConsumption_US increases by 1 unit, the
        Beef_Value_SlaughterMarket decreases by 7.055 units, holding other variables constant.

    -   Barley: The coefficient is -0.001, with a p-value of 0.082, indicating no significant relationship between Barley and
        Beef_Value_SlaughterMarket.

    -   SoyaBeans: The coefficient is 0.003, with a p-value of <0.001, indicating a significant positive relationship between
        SoyaBeans and Beef_Value_SlaughterMarket. As SoyaBeans increases by 1 unit, the Beef_Value_SlaughterMarket
        increases by 0.003 units, holding other variables constant.

#plots

### Regression – No Precipitation, No Avg Temperature, No Beef Production, No Maize, No Sorghum, No Barley

## Model Summary: 

The model summary indicates that the adjusted R-squared is 0.709, which means that approximately
70.9% of the variability in the Beef_Value_SlaughterMarket can be explained by the model with the given predictor
variables (BeefConsumption_US and SoyaBeans). The model's standard error of the estimate is 6.61327, which reflects
the average distance that the observed values fall from the regression line.

## ANOVA: 

The ANOVA table shows that the model is statistically significant at a <0.001 level. This means that there is a
significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor variables. The
F-value of 24.132 indicates that the model is a good fit to the data, as it is significantly different from a model with no
predictors.

## Coefficients: 

The coefficients table provides information about the relationship between each predictor variable and the
dependent variable (Beef_Value_SlaughterMarket).

    -   BeefConsumption_US: The coefficient is -5.840, with a p-value of <0.001, indicating a significant negative relationship
        between BeefConsumption_US and Beef_Value_SlaughterMarket. As BeefConsumption_US increases by 1 unit, the
        Beef_Value_SlaughterMarket decreases by 5.840 units, holding other variables constant.

    -   SoyaBeans: The coefficient is 0.002, with a p-value of <0.001, indicating a significant positive relationship between
        SoyaBeans and Beef_Value_SlaughterMarket. As SoyaBeans increases by 1 unit, the Beef_Value_SlaughterMarket 
        increases by 0.002 units, holding other variables constant.
        
This simplified model with only significant variables (BeefConsumption_US and SoyaBeans) explains about 70.9% of the
variability in the Beef_Value_SlaughterMarket.

#plots

___________________________________________

# Section IV: SPSS Stepwise Variable Removal

In this stepwise regression model, SoyaBeans was entered in the first step, and BeefConsumption_US was entered in the
second step, based on the specified criteria.

## Correlations: 

The Pearson Correlation table displays the correlations between the dependent variable (Beef_Value_SlaughterMarket) 
and each of the predictor variables. The significant correlations are with BeefConsumption_US (-0.637, p<0.001) and SoyaBeans (0.686, p<0.001).

## Model Summary:

    -   Step 1: In the first step, only SoyaBeans is included as a predictor. The adjusted R-squared is 0.441, which means that
                44.1% of the variability in the Beef_Value_SlaughterMarket can be explained by SoyaBeans alone.

    -   Step 2: In the second step, BeefConsumption_US is added as a predictor. The adjusted R-squared increases to 0.709,
                indicating that 70.9% of the variability in the Beef_Value_SlaughterMarket can be explained by both SoyaBeans and
                BeefConsumption_US.

## ANOVA:

The ANOVA table shows that both models are statistically significant at a <0.001 level. This indicates that
there is a significant relationship between the dependent variable (Beef_Value_SlaughterMarket) and the predictor
variables in both models.
 
## Coefficients:

    -   Step 1: The coefficient for SoyaBeans is 0.003 (p<0.001), indicating a significant positive relationship with
                Beef_Value_SlaughterMarket.

    -   Step 2: The coefficients for SoyaBeans and BeefConsumption_US are 0.002 (p<0.001) and -5.840 (p<0.001),
                respectively, indicating significant positive and negative relationships with Beef_Value_SlaughterMarket.

## Excluded Variables: 

This table shows the variables that were not included in the model, along with their p-values and
collinearity statistics. None of the excluded variables met the criteria for inclusion in the model.

## Collinearity Diagnostics: 

The collinearity diagnostics table indicates that multicollinearity is not a major concern in this
model. The variance inflation factors (VIF) for both predictor variables (SoyaBeans and BeefConsumption_US) are close
to 1, which is an acceptable level.

In conclusion, the stepwise regression analysis resulted in a model with two significant predictor variables, SoyaBeans
and BeefConsumption_US, which together explain about 70.9% of the variability in the Beef_Value_SlaughterMarket. 

#plots
___________________________________________

# Section V: Conclusion and Discussion

In both models, the significant relationships between the dependent variable and the two predictors (SoyaBeans and
BeefConsumption_US) are consistent, with SoyaBeans having a positive relationship and BeefConsumption_US having a
negative relationship. Overall, the two models have the same predictor variables and show similar results in terms of
adjusted R-squared values and the relationships between the dependent variable and predictors. The stepwise regression
model automated the process of selecting significant predictors, while the manual removal of variables allowed for a more
controlled approach. In this case, both methods led to the same conclusion.

## 1. An increase in the production of primary feed crops, such as maize and soya beans, leads to an increase in beef production.

## 2. Climatic factors, such as temperature and precipitation, have a direct impact on beef production.

## 3. Changes in consumer preferences and dietary habits can impact beef production.

Our analysis of the factors influencing the total value of beef at slaughter markets has revealed the complex interplay of
various variables, including crop production, climatic factors, cattle population, and meat consumption. By using a
stepwise regression model, we have identified the most significant factors and provided insights into their impact on beef
production. This knowledge can help stakeholders in the beef industry make informed decisions and implement strategies
to optimize production while addressing the challenges posed by changing consumer preferences, climate conditions, and
global food security concerns. It's important to consider that the model may not capture all the complexities and nuances
of the real-world situation. Although maize is essential for cattle production and climatic factors play a significant role in
crop growth, these variables were not found to be significant predictors of the Beef_Value_SlaughterMarket in the current
model. Given the knowledge that climatic factors play a role in crop production we should explore these interactions
further and compare models.
___________________________________________
##### References
___________________________________________
- United States Department of Agriculture 
- Food and Agriculture Organization of Nations (FAO)



