# CS_Grad_Admission
CS4602 Introduction to Machine Learning <br>
Final Project Proposal <br>
Team 23 <br>

| Name   	|      	| SID       	|
|--------	|------	|-----------	|
| 廖宏淇 	| Amy  	| 107062273 	|
| 郭冠廷 	| Mimi 	| 107062274 	|
| 陳宗佑 	| Lear 	| 107062374 	|

DDL: 11/6 (Friday)



## Abstract (Amy)

### Literature review
- https://medium.com/analytics-vidhya/a-fresh-look-at-graduate-admissions-dataset-d39e4d20803e (Mimi) <br>
  The research used a random forest model to study the relationship between the Chance of Admit and factors including GRE Score, TOEFL Score, the applied University Rating, SOP and LOR Strength, Undergraduate CGPA and Research Experience based on a graduate studies dataset for Indian students .
- https://towardsdatascience.com/graduate-admission-prediction-using-machine-learning-8e09ba1af359 (Amy)
- https://debarghyadas.com/writes/the-grad-school-statistics-we-never-had/ (Lear) <br>
  The author of the article analyses graduate admission in the U.S. with GPA, GRE (Verbal, Quant), Citizenship.

## Methodology

- Raw data (Lear)

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
    
  - https://www.kaggle.com/mohansacharya/graduate-admissions
  
    The data comtains some other attribute. e.g.

    - GRE Scores ( out of 340 )
    - TOEFL Scores ( out of 120 )
    - University Rating ( out of 5 )
    - Statement of Purpose and Letter of Recommendation Strength ( out of 5 )
    - Undergraduate GPA ( out of 10 )
    - Research Experience ( either 0 or 1 )
    - Chance of Admit ( ranging from 0 to 1 )
    

- Model (Mimi)
  The study plans to predict Chance of Admit with the probablity by using the raw data mentioned for the input. 
  Different models, including Bayesian, SVM and DNN, would be  
  - Input: Collected from Github
  - Output: [Admission/ Rejection/ Probably] + chance(%) 
  - Model: Bayes or SVM or DNN -> Shallow neural network (ensemble learning?)

## Planning Chart (Lear)

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
