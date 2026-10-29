# Education Inequality

> Education is a basic human right, and higher education is linked to better outcomes later in life. ACT scores are one of the qualifications that are reviewed for access to higher learning institutions. This project aims to examine the socioeconomic factors that contribute to high school student success on the ACT.

---

## Project Overview



- **Objective:** Use linear regression models to build an accurate prediction of ACT score and determine most influential predictors.
- **Domain:** Education
- **Key Techniques:** Linear Regression

---

## Project Structure

```
├── data/                 
	ACSDP1Y2016.DP03-2026-10-28T070459.csv 			#School Information
	EdGap_data_reformatted.xlsx				#EdGap Data
	education_clean.csv					#Cleaned version of School Information and Edgar
	/ducation_census.csv					#Cleaned data with census data
├── code/                 
	data_cleaning.ipynb 					#Code used to produced cleaned version of data
	education_data_code.ipynb				#Code used for analysis and visualizations
├── reports/              
	   education_report.pdf					# Generated reports and visualizations
├── requirements.txt     					# Dependencies
└── README.md             					# Project documentation
```

---

## Data

- **Source:** The primary data set is the EdGap data set from EdGap.org. This data set from 2016 includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district. The school information data is from the National Center for Education Statistics. This data set consists of basic identifying information about schools. US Census Bureau provided additional economic data.
- **Description:** Brief overview of the dataset features, size, and format
- **License:** Academic purposes only.

---

## Analysis

Run Notebooks in order of appearance. To reproduce the results, 'Run All' to run the code in the order it appears. If an error appears, it can usually be resolved by running all of the code above the error before re-running the cell. 

1. data_cleaning.ipynb contains the code used to clean the data. 
2. education_data_code.ipynb


---

## Results

From the analysis, it is clear the median income is a weak predictor of ACT score. Though it had a small root mean square error and mean absolute error which supports that there is a correlation. Transformations of the median income did not result in a significant change in correlation. Figure 1 shows the relationship between the median income and average ACT score. While the quadratic linear regression model provided a closer representation, it is still a weak correlation. Interestingly, there appears to be a much higher variation in ACT scores in school districts with lower median income than the high-income school districts.  

Of the seven selected socioeconomic indicators, percent of the students receiving free lunch had the highest correlation coefficient, indicating the strongest indicator of ACT score.  Though the correlation coefficient is negative, indicating an inverse relationship. The unemployment rate was the next highest predictor of ACT score, followed by percent of parents with college education. The former has an inverse relationship whereas the latter has a positive relationship. The two indicators from the US Census Economic data had low correlation coefficients: Percent receiving food stamps/SNAP and percent without health insurance.  

The multiple linear regression model with the seven indicators was able to predict average ACT score with a high R-squared value, indicating a good fit. However, the reduced model with only the top three predators was able to predict ACT score with similar levels of accuracy. The R-squared values for the two were the same to the hundredth's places.  

Percent of students receiving free lunch and unemployment rate are the two predictors with the strongest negative relationship with academic success, as measured by ACT score. Whereas percent of parents with a college degree has the highest positive relationship with average ACT score.  Other factors such as married parents, receiving food stamps, median income, and access to healthcare showed a weak influence on academic success. The regression model created with only the top three indicators did not have a substantially different correlation. 

---

## Authors

- Sophie Akin @sophsophiea GitHub.com/sophsophiea

---

## License

This project is intended for a class project only. 

---

## Acknowledgements

This project was created for DATA 5100 at Seattle University, based on course materials.
