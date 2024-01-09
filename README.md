# CardiovascularAnalysis

Cardiovascular Disease Prediction

Goal (or Thesis)

Cardiovascular disease is the leading cause of death globally, accounting for 31% of deaths. This project aims to predict the likelihood of an individual having cardiovascular disease using 11 potential factors. The dataset includes various features such as age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, maximum heart rate, exercise-induced angina, old peak, and the slope of peak exercise. Through statistical analysis and machine learning, we seek to determine if these factors can accurately predict the presence of cardiovascular disease.

Dataset Description

Size of the dataset: 918 rows and 12 columns
Column Names:
Age
Sex
ChestPainType
RestingBP
Cholesterol
FastingBS
RestingECG
MaxHR
ExerciseAngina
Oldpeak
ST_Slope
HeartDisease
Classification of each column:
Detailed classifications provided for each variable.
List of Discrete Values for Categorical Variables

Categorical Variables:
Sex:
Male
Female
ChestPainType:
ATA (Atypical Angina)
NAP (Non-anginal Pain)
ASY (Asymptomatic)
TA (Typical Angina)
RestingECG:
ST (ST-T wave abnormality)
LVH (Probable or definite left ventricular hypertrophy)
Normal
ExerciseAngina:
Yes
No
FastingBS:
0 (No)
1 (Yes)
ST_Slope:
Up (Upsloping)
Flat
Down (Downsloping)
HeartDisease:
0 (No)
1 (Yes)
Distribution of Discrete Variables
Frequency counts and modes are provided for each categorical variable.
Distribution of Quantitative Variables

Age (years):
Median: 54
Mean: 53.51
Standard Deviation: 9.43
Range: 49
RestingBP (mm Hg):
Median: 130
Mean: 132.40
Standard Deviation: 18.51
Range: 200
Cholesterol (mm/dl):
Median: 223
Mean: 198.80
Standard Deviation: 109.38
Range: 603
MaxHR (bpm):
Median: 138
Mean: 136.81
Standard Deviation: 25.46
Range: 142
Oldpeak (numeric ST):
Median: 0.6
Mean: 0.89
Standard Deviation: 1.07
Range: 8.8
Data Wrangling

No missing data found.
Data Range:
Anomalies in RestingBP and Cholesterol addressed by dropping one row and the Cholesterol predictor, respectively.
Data format is correct, and no duplicates were found.
Preliminary Statistical Analysis

Pearson correlation coefficients among quantitative data and their p-values are provided.
Further polynomial fits inconclusive due to the categorical nature of the target variable (HeartDisease).


Narration

● The world is fast globalizing, with business and technology sectors booming, aimed
at making everyday life easier. Unfortunately, with the high paychecks of this
lifestyle, there is also a sedentary and high-stress way of life. Paired with the
globalization of high-calorie foods in the form of “fast food”, we now see an increase
in the consumption of unhealthy but instantly filling foods everywhere. We’ve heard
of them; McDonalds, Taco Bell, KFC, you name it.
● With this advent, however, is the increase of unhealthy fats that clog up the heart and
lead to a brutal and fatal disease that has been on the increase everywhere. Formally
known as cardiovascular disease, or CVD, they are now the number one cause of
death globally; they take 17.9 million lives each year and account for 31% of deaths.
The most common form of CVD is heart attacks, and they make up 4 out of the 5
CVD deaths.
● With the increased advent of CVDs, it’s important that we use the same booming
technology to predict these heart diseases to help stop them from a medical
standpoint with a machine learning and data visualization medium. It can be done
across 11 mediums; age, sex, the type of chest pain, resting blood pressure levels,
cholesterol, fasting BS, resting ECG level, max heart rate (or HR), exercise-induced
angina, the old peak of exercise, and the slope of the old peak exercise. Using this to
predict the presence of heart disease, data analysis can be used to find the most
important features overall.
● The observations come from a worldwide bank, as this is a problem affecting
everyone worldwide; Cleveland, Hungary, Switzerland, Long Beach, and an external
Stalog dataset are being used as the focus. With 918 observations now, we plan to
filter the dataset accordingly, analyze it, create visualizations, and identify features
that can be of great use in stopping the spread of the CVD epidemic affecting the
world right now.
