# Project-1

The files that should be considered in this repository are as follows: Final_EDA_HD.ipynb, Honorable_Mentions.ipynb, Heart_Disease_Prediction.csv, and heart.csv. All of the other files on this repository are just check points/ideas we had along the way.

Final_EDA_HD.ipynb, Heart_Disease_Prediction.csv, and heart.csv are where you will be able to find all of the data that we though was necessary to answer our question for this project. 
Honorable_Mentions.ipynb is a file that shows some of the figures that we made and tests that we ran that we determined were not necessary to properly analyze our questoin. 

Althernative hypothesis: The factors that are attributed to heart disease will increase between the ages of 45-65.
Null hypothesis: The factors that are attributed to heart disease will not increase between the ages of 45-65.

Note: We are looking at factors that are commonly attributed to heart disease in regaurds to age, not these factors against heart disease itself.


Subset of 9 attributes we considered in our merged data set:
Age in years
Sex (0 = female, 1 = male)
Chest pain type (Value1: typical angina, Value2: atypical angina, Value3: non-anginal pain, Value4: asymptomatic)
BS (Blood Pressure) resting blood pressure (in mmHg)
Cholesterol (serum cholesterol in mg/dl)
FBS over 120 fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
Exercise Angina exercise induced angina (1 = yes, 0 = no)
Number of blood vessel Fluro number of major vessels (0-3) colored by fluoroscopy
Heart Disease (0 = Absent, 1 = Present)

Analysis:

Age vs Sex: The proportion of Sex remains fairly constant between both groups. There are more male than female patients in the dataset. 68% male to 32% female. 
Age vs FBS over 120: There is a slight increase of FBS over 120 in the age group 45-65 years. The percentage of FBS over 120 increases from 14.9% to 17.0% for the age group 45-65 years.
Age vs Exercise Angina: There is a slight but noticeable increase of Exercise Angina in the age group 45-65 years. The percentage of the presence of Exercise Angina increased from 32.9% to 35.6% for the age group 45-65 years.
Age vs Heart Disease presence: There is no significant difference between the two groups. There is a slight decrease of the presence of Heart Disease in the age group 45-65 years of 49.4% versus 49.7% in the other age group (less than 45 and greater than 65 years). 

Age vs Sex: There is nearly a 2 to 1 ratio skewed to male patients. This dataset has more male patients than female patients. This is the case for both groups. The mean age for both groups is similar. 
Age vs FBS over 120: FBS over 120 (orange boxes) occurs in a smaller range of ages compared to FBS under 120. It occurs at older ages starting at ~46 years. The mean age of the group with FBS over 120 is slightly older than the age group with FBS under 120. 
Age vs Exercise Angina: There is an outlier in the group including all ages in the dataset. Similarly to FBS over 120, Exercise Angina generally occurs at older ages compared to the control population. The mean age of exercise angina (presence) is slightly older than the absence of exercise angina for the entire age group. 
Age vs Heart Disease (absence or presence): The two groups almost mirror each other. However the mean age of both groups is slightly older in the absence of heart disease. 

Significant factors (control group):
Age has moderate positive correlation with number of vessels fluro (0.33).
Age has moderate-to-weak positive correlation with Blood Pressure (0.28).
Age has a weak positive correlation with Cholesterol (0.21).
Sex has a weak negative correlation with Cholesterol (-0.20).                             
We choose Females to have value 0 and males to have value 1: there is a weak correlation that females are more likely to have higher cholesterol than males. 

Significant factors:
Age has a weak positive correlation with Blood Pressure and Number of vessels fluro. (0.24 and 0.21, respectively)
Chest Pain type and Heart Disease presence has a weak positive correlation. (0.25)
Sex and Cholesterol has a weak-to-moderate negative correlation. Females are more likely to have higher cholesterol than males. (-0.27)

Results: T-Test Analysis on Heart Disease Factors vs Age

Methodology: Age groups were broken into two subsets. 
Ages 45 - 65
Ages less than 45 and ages greater than 65
Resulting P-Value from T-tests
Heart Disease (presence) vs Age: p-value = 0.8423
Cholesterol vs Age: p-value = 0.0299
Blood Pressure vs Age: p-value = 0.0158
FBS (fasting blood sugar) over 120 mg/dL vs Age: p-value = 0.0226
Exercise Angina vs Age: p-value = 0.0330
Sex vs Age: p-value = 0.9104
Chest pain type (0-4) vs Age: p-value = 0.9098
Number of Vessels Fluro vs Age: p-value = 0.0707

Conclusion:
After collecting and analyzing this dataset, we accept the alternative hypothesis and reject the null hypothesis that factors attributed to heart disease increase with ages 45-65. 
Cholesterol, Blood Pressure, FBS (fasting blood sugar) and Exercise Angina had p-values less than 0.05 when tested against the two age groups.

Note: there was not a clear relationship between the presence of heart disease and the different age groups which can partly be explained by stating the limitations of the dataset we used.

Data Limitation:
The UC Irvine study used only the data from patients that were referred to the Cleveland Clinic Foundation. This would imply that the data used was from patients with a risk for heart disease. The study did not include the general population. If it had, it more than likely would have impacted the results.

The dataset did not take into consideration other heart disease risk factors such as family history, race, ethnicity, income, smoking, or alcohol consumption.

The dataset is from a study that was done in 1988. A lot has changed since then, and the dataset does not represent the medical advancements that have increased physician’s knowledge of heart disease or the new tools for the diagnosis and treatment of this disease.

Data that we would like to see moving forward:
More data from people younger than 45 (specifically younger than 30)
More data from people older than 65
Heart attack count per person (how many total heart attacks an individual has had if they’ve had more than 1)
Better conclusions could be made if we looked at more data that focused on genetics 


