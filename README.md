
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
The Edgap dataset was obtained from Edgap.org —a platform that provides maps, visualizations, and resources to encourage discussion about the education gap in the United States. The platform offers access to data on various socioeconomic variables of interest, enabling analysis of factors within districts and individual schools. The EdGap dataset identifies schools only by their National ID. The ID alone does not provide information such as the school’s location, name, or type. To obtain more detailed information linked to these IDs, additional data were retrieved from the National Center for Education Statistics (NCES), the primary statistical agency of the U.S. Department of Education responsible for collecting, processing, and analyzing educational data. Through this source, we gathered further details about each school corresponding to its ID. In addition to the socioeconomic variables present in the EdGap dataset, it was also important to understand the influence of other socioeconomic factors. The variable we chose to study, in order to assess its relationship with ACT scores, was the number of full-time equivalent (FTE) teachers a school employs. This number was calculated by counting one full-time teacher as 1.0 and one part-time teacher as 0.5, meaning two part-time teachers are equivalent to one full-time teacher. The data was also retrieved from the National Center for Education Statistics(NCES) website.


Source: 
The data was obtained from:
- Edgap dataset: https://www.edgap.org/#4/37.71/-95.99
- fte_teachers and school information dataset: https://nces.ed.gov/ccd/elsi/

For reference to the datasets:
- school_information: https://www.dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&dl=0
- edGap_data: https://github.com/brian-fischer/DATA-5100/blob/main/EdGap_data.xlsx
- fte_teachers data: https://github.com/kembaoak/education/blob/main/data/ELSI_csv_export_6389617089029104698184.csv

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


Note: cleaning was done using the notebook - https://github.com/kembaoak/education/blob/main/code/Education_clean.ipynb

To perform exploratory data analysis:
- Import the clean data
- create correlation matrix to analyze relationship between predictor variables and ACT score.
- conduct single regression test
- conduction multiple regression test
- Understand the R^2, r, mean absolute error  values and what they imply for the variables


Exploratory Analyses was completed using notebook: https://github.com/kembaoak/education/blob/main/code/Ediucation_EDA.ipynb
  
Our findings indicate that out of all the socioeconomic predictors, the strongest predictor of the ACT scores was the percentage of students on reduced lunch(percent_lunch) variable. Other predicor variables such as the rate of unemployment, percentage of adult with a college degree, and the number of full time equivalent teachers also contributed to the variation in ACT score but not as significantly as percent_lunch. Note that we cannot establish a causal relationship given all the other confounding factors that must influence ACT scores. 

Requirements: 
# Core
NumPy - is a python library used for numerical operations, arrays, and mathematical calculations.  
Pandas - is a python library that provides data structures like DataFrames for data manipulation, cleaning, and aggregation.

# Visualization
matplotlib - A plotting library used to create static visualizations like line plots, bbar charts, and scatter plots. 
seaborn - is built on Matplotlib, used for advanced statistical data visualizations and improved aesthetics.
plotly - is a python package for data visualization. It is used to create interactive high quality charts, graphs and dashboards. 
#Dta Handling
openpyxl - is a python library used for reading, writing, and editing excel files - especially if it has the modern .xlsx format. 

# Machine Learning

statsmodels - used for statistical modelling and hypothesis testing, including t-tests, z-tests and regression analysis.
scikit-learn: is a python machine learning library used for machine learning algorithms like regression, classification, etc. 

# Jupyter & Development
jupyter notebook - An interactive environment for writing and executing Python code, organizaing, and documenting results. 
ipython - Provides an enchanced Python shells used in Jupyter Notebooks.

#Others
VS Code - is a free, open source code editor developed by Microsft. It is widely used for programming, data analysis, and development projects. 

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
