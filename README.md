# [Data Science] What Factors Affect Student Performance?

---- A feature & model selection project ----

Project start date: January 15th, 2018

### Directory Information
`data`:  raw data, cleaned data, and data table output.
`src`: project source codes.
`graphs`: visualizations for exploratory and explanatory analysis.
`reports`: analysis reports.

### Project Overview

To understand whether student performance in final grade is affected by student previous grades, demographic, social and school related information, I want to perform a linear regression model.

Instead of fitting 1 linear regression with no regularization, I apply different regularized linear regression methods and compare their result to the unregularized one. These methods include Lasso (L1 regularization), Ridge (L2 regularization), Elastic Net (L1 + L2 regularization). The comparison will suggest me the best model to help answer my question above.

### Data Description

Data used in this project is taken from the [Student Performance Data Set](http://archive.ics.uci.edu/ml/datasets/Student+Performance). It contains student achievement in secondary education of two Portuguese schools, along with their grades, demographic, social and school related features. The data was collected by using school reports and questionnaires.

The final dataset (after cleaning) has 32 features, with 382 observations in total. None of those observations has missing values.

To know more details about the features, please refer to this [README](https://github.com/hadinh1306/feat-select_student-performance/tree/master/data/raw_data).

To answer my question, I choose `G3` - the final grade as my response variables, and other 31 variables as my explanatory variables.

Since I decide to use Scikit-learn to fit models to my data and Scikit-learn Regression Models only understand numeric data, I transform text values of all categorical variables into numeric ones. See source code for cleaning data [here](https://github.com/hadinh1306/feat-select_student-performance/blob/master/src/clean.ipynb).

### How to run analysis and report

|   | Step                                                                                       | src | expected output path |
|---|--------------------------------------------------------------------------------------------|-----|-----------------|
| 1 | Download data from [here](http://archive.ics.uci.edu/ml/machine-learning-databases/00320/student.zip) |     |                 |
| 2 |  Merge and transform data for further use                                                                                          |  `clean.ipynb`  | ../data/cleaned _data/cleaned.csv            |
| 3 |  Exploratory Data Analysis                                                                                          |  `EDA.ipynb`   |  some images in ../graphs/      |
| 4 | Explanatory Analysis   | `model.ipynb` | ../data/analysis/model_score.csv and ../data/graphs/resid_plot.png |
| 5 |  Run report | `Final Report.ipynb`, which can be found in `reports` folder | | |

### Report

Link to [report](https://github.com/hadinh1306/feat-select_student-performance/blob/master/reports/Final%20Report.ipynb) with findings and analysis processes.
