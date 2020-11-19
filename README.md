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
  Many undergraduate students are struggling with graduate program admission in their final year. With limited amount of time and resource, it is unlikely to hand in numorous application. Therefore, it is important for them to decide on what schools and programs they are going to apply for carefully, as their chooses could greatly impact their future. Currently, however, these undergrads rely heavily on the results from their senoirs to decide what to apply, and there is not yet a functional application for them to see what field, within all the information they provide the school they are applying to, does each school value more. Therefore, the focus of this project to find a model that can predict the probability of a individual of getting an offer from a particular school. This way, students would be able to re-consider their applications and make the best decision out of it. 

## Objective
   This study hopes to develop a framework that help undergraduate students to get into their ideal graduate schools while saving their time and resources. In order to achieve this goal, the study consists of three key objectives. The first objective is regarding data analysis. With the two datasets available, data statistics, such as how the applicants data for each graduate school is distributed, is observed. Then, by deploying different machine learning models and evaluation their results, insights like the different category weighting are extracted and an estimation of Chance of Admit would be made. Lastly, we hope to provide a simple platform for users to input their information, such as their GRE score or undergraduate GPA, and display the probability of getting admitted, calculated by our models, to them.
   
   Objectives:
   1. Perform data analysis from existed application data
   2. Deploy models to predict the Chance of Admit percentage
   3. Provide a simple platform for student to use it
  


## Literature review
- **[A Fresh Look At The Graduate Admissions Dataset](https://medium.com/analytics-vidhya/a-fresh-look-at-graduate-admissions-dataset-d39e4d20803e)**
  
  link: https://medium.com/analytics-vidhya/a-fresh-look-at-graduate-admissions-dataset-d39e4d20803e <br>
  The research used a random forest model to study the relationship between the Chance of Admit and factors including GRE Score, Undergraduate CGPA, Research Experience and more based on a graduate study dataset for Indian students. 
  
  
- **[Graduate Admission Prediction Using Machine Learning](https://towardsdatascience.com/graduate-admission-prediction-using-machine-learning-8e09ba1af359)**
  
  link: https://towardsdatascience.com/graduate-admission-prediction-using-machine-learning-8e09ba1af359 <br>  
  This researchers used the RandomForestRegressor to find important features which are CGPA, GRE, and TOEFL score for graduate admission. 

_Both papers above are based on a [kaggle dataset](https://www.kaggle.com/mohansacharya/graduate-admissions), which did not provide any information on how they gather the data._
  
  
- **[The Grad School Admissions Statistics We Never Had](https://debarghyadas.com/writes/the-grad-school-statistics-we-never-had/)** 
  
  link: https://debarghyadas.com/writes/the-grad-school-statistics-we-never-had/ <br>
  The author of the article analyses graduate admission in the U.S. with GPA, GRE (Verbal, Quant), Citizenship.
  
  
- **[A Statistical Approach to Graduate Admissions’ Chance Prediction](https://link.springer.com/chapter/10.1007/978-981-15-2043-3_38#Abs1)**

  link: https://link.springer.com/chapter/10.1007/978-981-15-2043-3_38#Abs1 <br>
  This study deployed gradient boosting regressor model to analyze the relationship of university rating and student’s academic achievements, and computed performance error.
  
  
- **[Apriori Algorithm and Decision Tree Classification Methods to Mine Educational Data for Evaluating Graduate Admissions to US Universities](https://link.springer.com/chapter/10.1007/978-981-15-1632-0_12)**

  link: https://link.springer.com/chapter/10.1007/978-981-15-1632-0_12 <br>
  This study applied Apriori methods and Decision Tree Classification to outline the requirements for admissions to universities with top-, mid-, and lower ranking.
  
  
- **[Will I Get in? Modeling the Graduate Admission Process for American Universities](https://ieeexplore.ieee.org/document/7836726)** 

  link: https://ieeexplore.ieee.org/document/7836726 <br>
  The paper analyzed factors such as GPA, university reputation of a dataset more than 150,000 applications as a binary classification problem with latent variables that account for additional information. 


## Methodology

### Datasets

  There are two datasets used in the project (One from Kaggle. Another from GitHub).
  
- **[Gradcafe Data](https://github.com/deedy/gradcafe_data)**

  link 1: https://github.com/deedy/gradcafe_data (2006 - 2015) <br>
  link 2: https://github.com/karunk/Gradcafe-Computer-Science-Dataset (2014 - 2019) <br>
  The data was collected from a on-line graduate school applaction forum and clean by the owner of the GitHub repository.
  The stored attributes includes 


- **[University Graduate Admissions data set](https://cogcomp.seas.upenn.edu/page/resource_view/127)**

  link: https://cogcomp.seas.upenn.edu/page/resource_view/127 <br>
  This data set was collected for the graduate university admissions paper "Will I get in?" in late 2014. The data was scraped from edulix.com and is     presented here in csv format.


- **[\[Unreliable\]_Graduate Admission 2_](https://www.kaggle.com/mohansacharya/graduate-admissions)**

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
| Other Miscellaneous Details    	|       (Comment)      	|    ☑️   	|     ☑️     	|        	|
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
| SoP/LoR Strength               	|           5          	|        	|          	|    ☑️   	|

### Model <br>
  The study plans to predict the Chance of Admit with the probability in an ensemble learning approach. <br>
  Two models would be built and trained based on the two different datasets mentioned above. The third model would be using the outputs of the two former models to generate the final output. 
  <p align="center">
    <img width="460" height="300" src=./figure/model.png?raw=true>
  </p>
  
<!--- ![model](./figure/model.png?raw=true) --->

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
