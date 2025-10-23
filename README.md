
**Analysis of ACT Score and Socioeconomic factors**

The goal of this project is to explore the relationship between ACT Scores and several socioeconmic factors such as employment status, education level, marital status and whether one is in a lunch program at their educational institution. 

Project Overview
##Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.
The project analyzes the relationship between ACT scores and various scoioeconomic factos like  employment status, education level, marital status and whether one is in a lunch program at their educational institution across certain U.S districts. The data used includes dataset from  Edgap.org which includes data on socioeconomical factors that could impact ACT scores within a school's district and the average ACT scores for some schools around the U.S.

 

Objective: The goal is to identify how socioecomic conditions may impact/influence academic performance through ACT scores and provide a description of the trends analyzed. 

Domain: Education
Key Techniques: (e.g., Regression, Classification, Clustering, NLP, Time Series)
Project Structure
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation

Data
Source: 
school_information: https://www.dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&dl=0
edGap_data: https://github.com/brian-fischer/DATA-5100/blob/main/EdGap_data.xlsx
fte_teachers data: 
https://github.com/kembaoak/education/blob/main/data/ELSI_csv_export_6389617089029104698184.csv
Description: Brief overview of the dataset features, size, and format

Analysis
Before anylyzing, the data needs to be cleaned.

- import the datasets
- create a pairplot to analyze our dataset to ensure that relationships between variables exist before further analysis. 
- clean the data to ensure that data types within data sets are consistent.
- Replace NaN values using Impute Iterators for predictor variables.
- Remove/Replace ACT scores that are within the accepted range of 1 and 36.

- Provide the data set variables with descriptive names that are consistent.
- Merge our datasets using the key. (the above can be done before merging but make sure to give ensure key variable have consistent names before matching)
Results
- Use IterativeImputer to impute the missing values
- Export the data
To analyze:
- Import the clean data
- create correlation matrix to analyze relationship between predictor variables and ACT score.
- conduct single regression test
- conduction multiple regression test
- Understand the R^2, r, mean absolute error  values and what they imply for the variables
  
Our findings indicate that out of all the socioeconomic predictors, the strongest predictor of the ACT scores was the percentage of students on reduced lunch(percent_lunch) variable. Other predicor variables such as the rate of unemployment, percentage of adult with a college degree, and the number of full time equivalent teachers also contributed to the variation in ACT score but not as significantly as percent_lunch. Note that we cannot establish a causal relationship given all the other confounding factors that must influence ACT scores. 

Authors
Your Name -Edwin Okwor
License
This project is licensed under the MIT License - see the LICENSE file for details.

You are free to use, modify, and distribute this project for personal or commercial purposes,
as long as you include proper credit to the original author.

Acknowledgements
Tools/libraries used: Python, Jupyter Notebook, Pandas , NumPy, Matplotlib, Scikit-learn, VS Code Tutorials
Tutorials or papers referenced: None
Inspiration or collaborators: None
