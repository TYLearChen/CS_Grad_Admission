# CS_Grad_Admission
CS4602 Introduction to Machine Learning <br>
Final Project Proposal <br>
Team 23 <br>

| Name   	|      	| SID       	|
|--------	|------	|-----------	|
| 廖宏淇 	| Amy  	| 107062273 	|
| 郭冠廷 	| Mimi 	| 107062274 	|
| 陳宗佑 	| Lear 	| 107062374 	|




## Introduction

  We noticed that most of the undergraduate students are struggling with graduate program admission. Therefore, this project tries to find the model that can predict the probability of getting an offer. Our users can input their information such as their GRE score or undergraduate GPA, and the probability of getting admission will be displayed.

## Literature review
- https://medium.com/analytics-vidhya/a-fresh-look-at-graduate-admissions-dataset-d39e4d20803e <br>
  The research used a random forest model to study the relationship between the Chance of Admit and factors including GRE Score, Undergraduate CGPA, Research Experience and more based on a graduate study dataset for Indian students. However, the dataset, originated from kaggle, did not provide any information on how they gather the data.
- https://towardsdatascience.com/graduate-admission-prediction-using-machine-learning-8e09ba1af359 <br>
  This article used dataset from kaggle, (https://www.kaggle.com/mohansacharya/graduate-admissions), and used the RandomForestRegressor to find important features which are CGPA, GRE, and TOEFL score for graduate admission.
- https://debarghyadas.com/writes/the-grad-school-statistics-we-never-had/ <br>
  The author of the article analyses graduate admission in the U.S. with GPA, GRE (Verbal, Quant), Citizenship.  
- A Statistical Approach to Graduate Admissions’ Chance Prediction
  https://link.springer.com/chapter/10.1007/978-981-15-2043-3_38#Abs1
- Apriori Algorithm and Decision Tree Classification Methods to Mine Educational Data for Evaluating Graduate Admissions to US Universities
  https://link.springer.com/chapter/10.1007/978-981-15-1632-0_12
- Will I Get in? Modeling the Graduate Admission Process for American Universities
  https://ieeexplore.ieee.org/document/7836726


## Methodology

- Raw data

  There are two datasets used in the project (One from Kaggle. Another from GitHub).
  
  - https://github.com/deedy/gradcafe_data
    The data was collected from a on-line graduate school applaction forum and clean by the owner of the GitHub repository.
    The stored attributes includes 
    
    - uni_name
    - major
    - degree
    - season
    - decision
    - ugrad_gpa
    - gre_verbal
    - gre_quant
    - gre_writing
    
  - https://cogcomp.seas.upenn.edu/page/resource_view/127
    This data set was collected for the graduate university admissions paper "Will I get in?" in late 2014. The data was scraped from edulix.com and is     presented here in csv format.
    
    - Program
    - Term and Year
    - Major
    - University (will be) Attending
    - GRE_Quantitative
    - GRE_Verbal
    - GRE_AWA
    - TOEFL_Score
    - TOEFL_TWE (Essay)
    - IELTS_Score
    - Previous_University
    - Previous_Department
    - Grade
    - Topper's Grade
    - Grade Scale
    - Industrial Experience
    - Internship Experience
    - Research Experience
    - Conference Publications
    - Journal Publications
    - Type of Finance Docs
    - Type of Financial Aid
    - Amount
    - Undergraduate Arrears
    - Applied University
    - Destination Country
    - Applied Visa Type
    - Visa Consulate City
    - Appointment Date
    - Decision
    - Other Miscellaneous Details
    
    
  - **[unreliable]** https://www.kaggle.com/mohansacharya/graduate-admissions
    The data comtains some other attribute. e.g. GRE, TOEFL, Univ Rating, SoP or LoR Strength, GPA, Research Exp, Chance of Admit
    

- Model <br>
  The study plans to predict the Chance of Admit with the probability in an ensemble learning approach. <br>
  Two models would be built and trained based on the two different datasets mentioned above. The third model would be using the outputs of the two former models to generate the final output. 

## Planning Chart

|           Tasks 	|             Sub Task 	| 6.Nov 	| 12.Nov 	| ?.Nov 	| 26.Nov 	| 10.Dec 	| 20.Dec 	| 10.Jan 	|
|----------------:	|---------------------:	|:-----:	|:------:	|:-----:	|:------:	|:------:	|:------:	|:------:	|
|     1. Proposal 	|                      	|       	|        	|       	|        	|        	|        	|        	|
|                 	|      1.1 First Draft 	|   ☑️   	|        	|       	|        	|        	|        	|        	|
|                 	|     1.2 Second Draft 	|       	|    ☑️   	|       	|        	|        	|        	|        	|
|                 	|      1.3 Final Draft 	|       	|        	|   ☑️   	|        	|        	|        	|        	|
|        2. Model 	|                      	|       	|        	|       	|        	|        	|        	|        	|
|                 	|     2.1 Loading data 	|       	|        	|       	|    ☑️   	|        	|        	|        	|
|                 	|              2.2 SVM 	|       	|        	|       	|    ☑️   	|        	|        	|        	|
|                 	|              2.3 ANN 	|       	|        	|       	|    ☑️   	|        	|        	|        	|
|                 	| 2.4 Combining models 	|       	|        	|       	|        	|    ☑️   	|        	|        	|
|       3. Report 	|                      	|       	|        	|       	|        	|        	|    ☑️   	|        	|
| 4. Presentation 	|                      	|       	|        	|       	|        	|        	|        	|    ☑️   	|
