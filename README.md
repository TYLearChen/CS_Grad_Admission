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

### Raw data

  There are two datasets used in the project (One from Kaggle. Another from GitHub).
  
- **Gradcafe Data**

  link: https://github.com/deedy/gradcafe_data <br>
  The data was collected from a on-line graduate school applaction forum and clean by the owner of the GitHub repository.
  The stored attributes includes 

- **University Graduate Admissions data set**

  link: https://cogcomp.seas.upenn.edu/page/resource_view/127 <br>
  This data set was collected for the graduate university admissions paper "Will I get in?" in late 2014. The data was scraped from edulix.com and is     presented here in csv format.

- **[unreliable]** Graduate Admission 2

  link: https://www.kaggle.com/mohansacharya/graduate-admissions <br>
  The data comtains some other attribute. e.g. GRE, TOEFL, Univ Rating, SoP or LoR Strength, GPA, Research Exp, Chance of Admit

| Datasets                       	|         e.g.         	| Edulix 	| Gradcafe 	| Kaggle 	|
|--------------------------------	|:--------------------:	|:------:	|:--------:	|:------:	|
| Result                         	|       Admitted       	|    ☑️   	|     ☑️    	|    ☑️   	|
| Applied University             	|         NTHU         	|    ☑️   	|     ☑️    	|        	|
| Home country/status            	| Taiwan/International 	|    ☑️   	|     ☑️    	|        	|
| Program                        	|          MS          	|    ☑️   	|     ☑️    	|    ☑️   	|
| Term and Year                  	|      Spring 2016     	|    ☑️   	|     ☑️    	|        	|
| Major                          	|          CS          	|    ☑️   	|     ☑️    	|    ☑️   	|
| GRE(Q&V)                       	|          170         	|    ☑️   	|     ☑️    	|    ☑️   	|
| GRE(AWA)                       	|          170         	|    ☑️   	|     ☑️    	|    ☑️   	|
| Grade                          	|          99          	|    ☑️   	|     ☑️    	|    ☑️   	|
| Topper's Grade                 	|          99          	|    ☑️   	|          	|        	|
| Grade Scale                    	|          100         	|    ☑️   	|          	|        	|
| University (will be) Attending 	|         NTHU         	|    ☑️   	|          	|        	|
| TOEFL(Score)                   	|          120         	|    ☑️   	|          	|    ☑️   	|
| IELTS                          	|           9          	|    ☑️   	|          	|        	|
| Previous_University            	|         NTHU         	|    ☑️   	|          	|        	|
| Previous_Department            	|          CS          	|    ☑️   	|          	|        	|
| Industrial Exp                 	|        1 Year        	|    ☑️   	|          	|        	|
| Internship Exp                 	|        1 Year        	|    ☑️   	|          	|        	|
| Research Exp                   	|        1 Year        	|    ☑️   	|          	|    ☑️   	|
| Conference Publications        	|           2          	|    ☑️   	|          	|        	|
| Journal Publications           	|           2          	|    ☑️   	|          	|        	|
| Destination Country            	|        Taiwan        	|    ☑️   	|          	|        	|
| Other Miscellaneous Details    	|       (Comment)      	|    ☑️   	|          	|        	|
| SoP/LoR Strength               	|           5          	|        	|          	|    ☑️   	|

### Model <br>
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
