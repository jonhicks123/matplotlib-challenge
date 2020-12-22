# Pymaceuticals

#### Background of the Study

Acting as a senior data analyst at a pharmaceutical company, I analyzed the data of a study containing 249 mice which were identified with SCC tumor growth. The mice were treated  through a variety of drug regimens over the course of 45 days, and their tumor developments were observed and measured to identify the rate of tumor reductions as well as the effectiveness of the drug regimen. Pymaceuticals' drug of interest is Capomulin, so the main purpose of this study was to compare the effectiveness of other treatment regimens to see if any of them should be further researched and tested. 

## Observations and Insights

- It is observable that the size of the mouse has a strong correlation to the average tumor size, as the scatter plots show that heavier mice had larger average tumor volumes compared to mice with lower weights. As for the 45 day duration of testing, there were no mice out of the sample selection that got rid of the tumor entirely. If the testing duration were to be extended, it would be insightful to see if any of the drug regimens were able to eradicate the tumors from any of the mice.
  
- As for the drug regimens which were focused largely towards the end of the analysis, Capomulin and Ramicane prove to be much more effective as opposed to Infubinol and Ceftamine, and are rather similar in comparision. The only drug regimen in this particular section of the analysis that had outliers was Infubinol, though it only contained one outlier. It can be concluded that Ramicane is another great drug regimen that Pymaceuticals should use alongside Capomulin. Something that should be researched further would be the other drug regimens, and whether or not any of them are as successful in reducing tumor size as Capomulin and Ramicane.
  
- The sample size was split almost evenly between female and male mice, with male mice at 51% of the sample size and females at 49%. Something that would be interesting to analyze would be the reduction rate of males compared to females to see whether males and females had relatively similar tumor-size reduction rates or if one gender specifically had better succes than the other.

### Process of the Analysis

Joining both datasets and checking to see if any mice had duplicate time points, and removing any mice that did by dropping the mouse ID from the data. Only 1 mouse had duplicate timepoints, so the cleaned dataset used for the study consisted of 248 mice.

With the cleaned data, I conducted the following tasks:

- Generate a summary statistics table which consists of the mean, median, variance, standard deviation, and SEM of the tumor volume across each drug regimen.

- Create a bar plot showing the total number of measurements taken for each treatment regimen across the duration of the study. I created 2 identical bar plots by using Panda's DataFrame.plot method as well as Matplotlib's pyplot method.

- Created a pie plot showing the percentage of mice in the study which were male and female. I created 2 identical pie plots by using Panda's DataFrame.plot method as well as Matplotlib's pyplot method.

- Narrowed the data down to four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. With this data, I calculated the final tumor volume of each mouse, the quartiles, and IQR to check for outliers across the treatment regimens.

- Create a box and whisker plot containing the final tumor volume for all four treatment regimens using Matplotlib, and highlighted outliers in the plot by applying a custom color and style to them.

- Selected one random mouse that was treated with Capomulin and crafted a line plot which compared the time point vs. tumor volume for that specific mouse in order to see the effectiveness of the treatment regimen on a single mouse.

- To conclude the analysis, I crafted a scatter plot showing mouse weight vs. average tumor volume for the Capomulin treatment regimen. After creating this scatter plot, I calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment, and then added the regression line to the scatter plot.
