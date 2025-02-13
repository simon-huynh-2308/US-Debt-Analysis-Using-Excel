# US Debt Tracker Project

### Scenario: 
#### You were hired by a small debt agency in Washing DC that specializes in analyzing and forecasting public and private market debt. The US Government has requested an analysis of their public and governmental debt to answer some specific questions.

### Data Dictionary:
#### Debt Held by the Public: The portion of the US public debt that is held by individuals, corporations, foreign government
#### Intragovernmental Holdings: The portion of US public debt that is held by other US government agencies
#### Total Public Debt Outstanding: The sum of the debt held by the public and intragovernmental holdings.

### Questions:

#### 1. What was the Yearly Debt Percentage Increase for each year compared to the previous year?
#### 2. Which month historically have see the highest/ lowest increase in Total Debt?
#### 3. What is the projected growth of the publicly held debt in the next few years?

### Data Cleaning Process:

#### Purpose: The goal of cleaning data is because of the current raw dataset is not ideal for using Pivot Table with more than 7000 columns.

#### Process:
##### - Perform Transpose to flip the rows and columns. The dataset now is adjusted from vertical headings to horizontal headings.
##### - Format the cells to enhance visibility
##### - Apply Filter into the dataset
##### - Delete the blank rows
##### - Perform Ctr+H to replace Null values with Nothing 
##### - Adjust the values from Scientific Notation to Number 

### Questions 1:

#### For the purpose of this question, the last day of each year will selected to calculate the yearly debt percentage change. However, there are only 2 months in 2023, so the last day in Februry will be selected. The period year selected in this question will be 8 years (2015-2023).

#### The final day is the final amount of debt for both public, intragovernmental holding, and total public debt outstanding for each year. These values will be used to calculate the yearly debt percentage change for each year compared to the previous year.

#### The calculation is performed by subtracting the values of the current year from the previous year's values, then dividing the result by the previous year's values to determine the percentage change of Debt Held by the Public, Intragovernmental Holdings and Total Public Debt Outstanding.

#### Visualization: A Line Chart is created for Visualization

#### Insights:
##### - For the Total Public Debt Outstanding, in 2016 - 2019, the average increase was around 5%
##### - In 2020, there is a large spike that is most likely caused by the pandemic responses in the US


### Question 2:







