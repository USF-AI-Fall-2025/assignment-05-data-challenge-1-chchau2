# x62-data-challenge-student-pathways

__Part 1 Data Exploration:__

**Data Quality** 
Below are each column and their datatypes. The dataset consists of a mixture of objects and floats. 	
Data columns (total 11 columns):
     Column              Non-Null Count  Dtype  
---  ------              --------------  -----  
 0   DISTRICT_TYPE       20705 non-null  object 
 1   DISTRICT_NAME       20705 non-null  object 
 2   DISTRICT_CODE       17960 non-null  float64
 3   ACADEMIC_YEAR       20705 non-null  object 
 4   DEMO_CATEGORY       20705 non-null  object 
 5   STUDENT_POPULATION  20705 non-null  object 
 6   AWARD_CATEGORY      20705 non-null  object 
 7   WAGE_YEAR1          20705 non-null  float64
 8   WAGE_YEAR2          20705 non-null  float64
 9   WAGE_YEAR3          20705 non-null  float64
 10  WAGE_YEAR4          20705 non-null  float64

Most columns are complete, with DISTRICT_CODE being the exception. There are 2745 missing entries in the district code column.

DISTRICT_TYPE            0
DISTRICT_NAME            0
DISTRICT_CODE         2745
ACADEMIC_YEAR            0
DEMO_CATEGORY            0
STUDENT_POPULATION       0
AWARD_CATEGORY           0
WAGE_YEAR1               0
WAGE_YEAR2               0
WAGE_YEAR3               0
WAGE_YEAR4               0
dtype: int64


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

DISTRICT_CODE ranges roughly from 110,000 to 5.8 million. The WAGE columns range roughly from 0 to 150,000, with means between about 4,400 and 8,500. See below:
	
	DISTRICT_CODE    WAGE_YEAR1     WAGE_YEAR2     WAGE_YEAR3  
count   1.796000e+04  20705.000000   20705.000000   20705.000000   
mean    3.041331e+06   4476.106834    6075.533253    7310.831635   
std     1.583286e+06  11944.502346   16140.916903   19158.203471   
min     1.100170e+05      0.000000       0.000000       0.000000   
25%     1.864089e+06      0.000000       0.000000       0.000000   
50%     3.166852e+06      0.000000       0.000000       0.000000   
75%     4.277214e+06      0.000000       0.000000       0.000000   
max     5.872769e+06  97993.000000  132847.000000  146728.000000   

          WAGE_YEAR4  
count   20705.000000  
mean     8530.890413  
std     22106.663179  
min         0.000000  
25%         0.000000  
50%         0.000000  
75%         0.000000  
max    153910.000000 

Histograms show that all wage columns are clustered around 0 with a long right tail. This makes the data for wages skewed right, not normally distributed.

**Semantics**
Each column in the data represents information about a school district, or something about the school population. DISTRICT_TYPE, DISTRICT_NAME, and DISTRICT_CODE describe the kind of district, the name of it, and its unique identifier. ACADEMIC_YEAR indicates the academic year, 2018-2019. DEMO_CATEGORY and STUDENT_POPULATION describe the demographic subgroups of a student, such as race, foster status, homeless status, and gender. AWARD_CATEGORY refers to the type of credential earned. The four wage columns show the average annual wage each year after graduating. 

Using a heatmap to look at numeric relations, wage years 1-4 are strongly related to each other, while district code has no relation with them. 
	


	
