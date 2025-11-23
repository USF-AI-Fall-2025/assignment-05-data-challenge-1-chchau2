# x62-data-challenge-student-pathways

__Part 1 Data Exploration:__
Code found inside jupyter notebook can be run to find how these results were concluded. Screenshots provided.

**Data Quality** 

Below are each column and their datatypes. The dataset consists of a mixture of objects and floats. DISTRICT_TYPE, DISTRICT_NAME, ACADEMIC_YEAR, DEMO_CATEGORY, STUDENT_POPULATION, and AWARD_CATEGORY are object types which means that they are categorical, while the rest are floats, which means they are numeric.

![data types](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/data%20types.png)

Almost all data columns are complete, with DISTRICT_CODE being the exception. There are 2745 missing entries in the district code column.

![chart](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/missing%20info%20by%20column.png)
**Range**

The categorical columns are DISTRICT_TYPE, DISTRICT_NAME, ACADEMIC_YEAR, DEMO_CATEGORY, STUDENT_POPULATION, and AWARD_CATEGORY. 

DISTRICT_TYPE has unique values ['School District' 'Legislative District' 'All']. 

DISTRICT_NAME has unique values['Duarte Unified' 'Coronado Unified' 'Gilroy Unified' 'Pleasant Valley'
 	'Senate District 15' 'Adelanto Elementary' 'Assembly 
District 56'
'Klamath-Trinity Joint Unified' 'Modoc Joint Unified'
 	'Healdsburg Unified']

ACADEMIC_YEAR has unique values['2018-2019']

DEMO_CATEGORY has unique values ['Race' 'Homeless Status' 'All' 'Foster Status' 'Gender']

STUDENT_POPULATION has unique values 
['None Reported' 'Black or African American'
'Did Not Experience Homelessness in K-12'
 'American Indian or Alaska Native'
 'Native Hawaiian or Other Pacific Islander' 'All' 'Two or More Races'
 'Foster Youth' 'Female' 'White']

AWARD_CATEGORY has unique values
["Bachelor's Degree - Did Not Transfer" 'Associate Degree'
 'Community College Certificate' "Bachelor's Degree - Transferred"]

DISTRICT_CODE ranges roughly from 110,000 to 5.8 million. The WAGE columns range roughly from 0 to 150,000, with means between about 4,400 and 8,500. See screenshot:

![range](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/range.png)

Histograms show that all wage columns are clustered around 0 with a long right tail. This makes the data for wages skewed right, not normally distributed. See screenshot:

![histogram](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/numeric%20column%20distribution.png)

**Semantics**

Each column in the data represents information about a school district, or something about the school population. DISTRICT_TYPE, DISTRICT_NAME, and DISTRICT_CODE describe the kind of district, the name of it, and its unique identifier. ACADEMIC_YEAR indicates the academic year, 2018-2019. DEMO_CATEGORY and STUDENT_POPULATION describe the demographic subgroups of a student, such as race, foster status, homeless status, and gender. AWARD_CATEGORY refers to the type of credential earned. The four wage columns show the average annual wage each year after graduating. 

Using a heatmap to look at numeric relations, wage years 1-4 are strongly related to each other, while district code has no relation with them. See screenshot below:

![Heatmap](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/numeric%20vs%20numeric.png)
	

I also compared WAGE_YEAR4 with DISTRICT_NAME, AWARD_TYPE, and DEMO_CATEGORY. 

For DISTRICT_NAME, Legislative Districts have much higher average wages than School Districts. The “all” category has the highest mean overall because it includes multiple district types combined. When looking at the actual district types, Legislative Districts show much higher wages.

For AWARD_TYPE, The Bachelors Degree shows much higher wages compared to the other award categories. Associate Degree, Bachelor with transfer, and Community College all have very mean wages, meaning that they earned a lot less on average.

Screenshot below:
![numeric vs categorical](https://github.com/USF-AI-Fall-2025/assignment-05-data-challenge-1-chchau2/blob/main/numeric%20vs%20categorical.png)
