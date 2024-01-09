# CardiovascularAnalysis

Goal (or Thesis)

Cardiovascular disease is the leading cause of death around the world. If we are able to predict
whether an individual will have cardiovascular disease, it can save numerous lives. This dataset
consists of 11 factors that potentially predict heart failure: age, sex, chest pain type, resting blood
pressure, cholesterol, fasting blood sugar, resting ECG, maximum heart rate, exercise-induced
angina, old peak, and the slope of peak exercise. Using statistics and machine learning, this
project aims to determine if these factors can accurately predict whether an individual will have
cardiovascular disease.

## Description of the Dataset
● Size of the dataset
○ 918 rows and 12 columns
● Column Names
○ Age
○ Sex
○ ChestPainType
○ RestingBP
○ Cholesterol
○ FastingBS
○ RestingECG
○ MaxHR
○ ExerciseAngina
○ Oldpeak
○ ST_Slope
○ HeartDisease
● Classification of each column
○ Age: Discrete
○ Sex: Categorical
○ ChestPainType: Ordinal
○ RestingBP: Continuous
○ Cholesterol: Continuous
○ FastingBS: Categorical
○ RestingECG: Ordinal
○ MaxHR: Discrete
○ ExerciseAngina: Categorical
○ Oldpeak: Continuous
○ ST_Slope: Categorical
○ HeartDisease: Ordinal

## List of Discrete Values for Categorical Variables
The categorical variables in the dataset have the following discrete values:
● Sex
○ Male
○ Female
● ChestPainType
○ ATA (Atypical Angina)
○ NAP (Non-anginal Pain)
○ ASY (Asymptomatic)
○ TA (Typical Angina)
● RestingECG
○ ST (the person has ST-T wave abnormality)
○ LVH (showing probable or definite left ventricular hypertrophy by Estes'
criteria)
○ Normal
● ExerciseAngina
○ Yes
○ No
● FastingBS
○ 0 (No)
○ 1 (Yes)
● ST_Slope
○ Up (upsloping)
○ Flat
○ Down (downsloping)
● HeartDisease
○ 0 (No)
○ 1 (Yes)
● Distribution of Discrete Variables
Variable Frequency Count Mode
Sex Male - 725
Female - 193
Male
ChestPainType ASY - 496
NAP - 203
ATA - 173
TA - 46
ASY
RestingECG Normal - 552
LVH - 188
ST - 178
Normal
Exercise Angina No - 547
Yes - 371
No
FastingBS 0 (No) - 704
1 (Yes) - 214
0 (No)
ST_Slope Flat - 460
Up - 395
Down - 63
Flat
HeartDisease 0 (No) - 508
1 (Yes) - 410
0 (No)
● Distribution of Quantitative Variables
Age (years) RestingBP
(mm Hg)
Cholesterol
(mm/dl)
MaxHR
(bpm)
Oldpeak
(numeric
ST)
median 54 130 223 138 0.6
mean 53.510893 132.396514 198.799564 136.809368 0.887364
std 9.432617 18.514154 109.384145 25.460334 1.066570
range 49 200 603 142 8.8
Data Wrangling
● No missing data was found
● Data Range:
○ Two anomalies were found. RestingBP has one entry that is 0, and Cholesterol
has 172 entries that are 0. This isn’t possible and must have been an error during
compilation or an occurrence of missing survey data. To combat this, we have
decided to do the following:
■ Drop the row that has RestingBP as 0; dropping one row won’t skew the
analysis
■ Dropping Cholesterol as a predictor. 172 entries is a significant portion of
the dataset, and manipulating or dropping the rows may lead to
inaccuracies or biases during prediction. We also found that Cholestrol has
not been classified as either HDL (high-density lipoprotein) or LDL
(low-density lipoprotein). This is crucial information that is lacking
because high levels of LDL cholesterol are highly correlated with an
increased risk for heart disease, but the same correlation is not applicable
for HDL. Our data contains a variable that provides no distinction between
these two types of Cholesterol, making it a much less reliable predictor.
Hence, we have decided to drop it.
● All data is in the correct format, and no duplicates were found.
Preliminary Statistical Analysis
● Determination of the Pearson correlation coefficient among quantitative data (with
respect to the target variable, HeartDisease)
Variable Coefficient P-value
Age 0.2820117259633894 3.1608374545676735e-18
RestingBP 0.1179900056203317 0.0003427865820658028
FastingBS 0.2679936968421689 1.5089277260441325e-16
MaxHR -0.4014096143659478 8.044072537845721e-37
Oldpeak 0.40363801551695416 3.0042742414205553e-37
● Due to the fact that our target variable, HeartDisease, is categorical, the
preliminary analysis of further polynomial fits (quadratic or cubic) is
inconclusive. Hence, we might explore this later on during model building, with
different possibilities aside from OLS regression, to see if squaring or cubing the
variables might help predict HeartDisease more accurately.
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
