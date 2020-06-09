# Students’ Early Attrition Modelling for Clearwater State University

## Project Description 
Clearwater State University offers a wide variety of degree programs, from online degrees to a doctorate in education.
Programs are offered in the streams of the arts, education, business & nursing.
Some key strategic goals of the University are:

• Increase enrolment of students  
• Improve retention, progression and graduation rates  
• Recruit better academically qualified undergraduate and graduate students  
• Increase external funding and recognition  

Leverage data on student demographic profile, course preferences, performance record, grades, financial background, financial aid and other application information to:

1. Identify key drivers of early student attrition
2. Build a predictive model to identify students with higher early attrition risk
3. Recommend appropriate interventions based on the analysis

## Project Overview 
* Divided the dataset based on attributes indicating:
    * financial backgroung of the Student  
    * Student performance
    * demographic data
* EDA of each dataset  
* Featured engineered some of the columns   
* Concatenation of all the subgroup dataset into one dataset  
* Cross Validation among different models  
* Building model  
* Hypertuning the parameters and rebuilding the model  
* Conclusion 

## Resources Used  
Python Version : 3.8  
Packages : pandas, numpy, sklearn, matplotlib, seaborn, plotly, cufflinks  
Reference and article : Google  
Project Motivation : [https://www.youtube.com/user/krishnaik06]  
Presentation inspiration: [http://www.Slideshare.net]   


## Exploratory Data Analysis :
### Student demographic data analysis :
I looked into demographic factors of both student and university which influence the student for continuing their studies.

Some of my findings :  

![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/hostel_choise.png)

![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/hostel_choise_returned.png)

![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/background.png)

### Student Performance Record Analysis :
The key driving factor for student's early attrition is their academic performance before and after entering into college  

Some of my findings :

![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/corr.png)
![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/perfm.png)

### Financial Indicators Analysis :
I looked into student's family contributions and university involvement to help financially weak students  

Some of my findings :

![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/family_cont.png)

## Feature Engineering
* Checked the cardinality of categorical variables
* Encoded those categorical variable labels whose frequency were less than 80 with 'Miscellaneous' 
* Made column First term status from FIRST_TERM_ATTEMPT_HRS and encoded with string
* Made column Second term status from SECOND_TERM_ATTEMPT_HRS and encoded with string
* Removed columns having lots of missing data
* Encoded FATHER_HI_EDU_DESC, MOTHER_HI_EDU_DESC missing values with Other/Unknown'
* Get the dummy varaible of categorical columns

## Cross Validation
Performed 10 fold cross validation with average accuracy as scoring parameter among 4 different models  
#### Models with average accuracy score :
* **Random Forest Classifier** - 0.8170588235294117   
* **Gradient Boosting Classifier** - 0.826764705882353  
* **XGB Classifier** - 0.8102941176470588  
* **Logistic Regression** - 0.7873529411764706  

#### Clearly Gradient boost outperformed the other models 

## Model building
First I split the dataset into train and test, then i performed ML model building and trained the model using engineered dataset
### Performance 
![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/ML_perfm.png)
## Tuning Hyper parameters
I found out the best parameters of my ML model using Gridsearchcv  
### Best Parametes :
* max_depth : 3  
* max_features : sqrt  
* min_samples_split : 3  
* n_estimators : 142  
* subsample : 0.75
### Performance with configuring best parameters :  
![alt text](https://github.com/prashantlal56/Student_Attrition_rate/blob/master/Project%20Pics/ML_perfm_tp.png)

## Conclusion and appropriate interventions based on the analysis
* ##### Those student who did not attempt or not completed second term are more prone to leave the university.  
  * Grand extra time period to complete both first and second terms
  * Put a congratulation prize for those student who completes both the terms of first year
* ##### Student with high GPA as well as high test entrance score are more interested in further study.  
  * Give scholarship to those student who are good in their academic curriculums 
* ##### Some of the course fee are high as student are leaving because of less family contribution.
  * Involve government and other organization to invest in the university
  * Support middle class and lower class background student by organizing a charity fund event where people are asked to voluntary contribute for the great benefits.
* ##### Student age also matter as most of the student are of 18 years old.
  * Make course duration more flexible such that student don’t have to worry about their age 
* ##### There are lots of Major subject where fraction ratio of not returning for second year is greater than 0.2.
  * Make the subject more interesting
  * Relate some real life example with the subject
  * Adopt new learning technology such as Virtual reality
  * Invite more other university’s professor as visiting professor so that knowledge can be shared among student
  * Collaborate with other state or country university 
  * Send Student to other university in student exchange programs 
* ##### Parents with higher education level are supporting their son/daughter more financially. This is not the case for less educated parents.
  * Advertising plays the key role here
  * Make people aware of the diverse as well as affordable course offered by university.
  * Print advertisement in the news paper
  * make pamphlets 
  * digital advertisement
  * Organise event to showcase the university etc.

#### Beside that
* ###### Introduce current trending most demanded subject.
* ###### Drop those program where student admission rate is very low
* ###### Lower course fee of some of the most demanded subject if possible.
* ###### Add extra curricular activity with the regular course as a refreshment program for student 
* ###### Invest in infrastructure to provide better facility to the student 
* ###### Involve industry expert  people to share the experience knowledge among the student
* ###### Tie up with some of the organization so that student get an exposure to the industry.
* ###### Organize course related workshop to make student more involve in their respective subject




 
  
  
